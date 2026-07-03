---
title: "Week 11 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Fulfill the role of **API Contract QA** in the **CloudBrief** project — an automated tech news collection & summarization system on AWS.
* Write automated tests (unit tests, integration tests) and build a Postman collection for demo purposes.
* Perform security audits (SSRF, XXE, XSS, API Key leakage) and finalize API documentation.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Lab 3: Transforming data with Glue: <br>&emsp; + Data Validation and ETL: Use AWS Glue to clean, validate, and transform data. <br>&emsp; + Incremental Data Processing with Hudi: Apply Apache Hudi to handle upsert/delete operations on S3. <br> - Lab 4: Query and Visualize: <br>&emsp; + Data Analysis: Query S3 data using Athena and build interactive dashboards with QuickSight. <br>&emsp; + Advanced Athena: Use Federated query to access various data sources and integrate with SageMaker for predictions. | 06/29/2026 | 06/29/2026      | <https://cloudjourney.awsstudygroup.com/>  |
| 3   | - Lab 5: Data Lake Automation: <br>&emsp; + Basic Lake Formation: Register data lake locations, set up Data Catalog, and grant fine-grained permissions. <br>&emsp; + Apply Lake Formation: Configure security and manage access for Hudi, Iceberg, and Delta Tables. <br> - Bonus Lab: Glue DataBrew: <br>&emsp; + Use Glue DataBrew for visual data preparation and cleaning without writing code. | 06/30/2026 | 06/30/2026      | https://cloudjourney.awsstudygroup.com/>  |
| 4   | <br>&emsp; + Install Bun 1.3.x, run `bun install`, `bun run build`, `bun run test` successfully <br>&emsp; + Copy `backend/.env.example` → `backend/.env` <br>&emsp; + Collaborate with team (`ReinaMacCredy`, `RyugaRuki`) to align all `/api/v1/*` routes, JSON schemas, and article status definitions (`PENDING_CONTENT`, `CONTENT_FAILED`, `SUMMARY_FAILED`, `SUMMARIZED`) <br>&emsp; + Review `contracts/src/index.ts`, `frontend/lib/cloudbrief-mocks.ts`, `backend/src/app/routes/v1.ts` | 07/01/2026 | 07/01/2026   
| 5   | <br>&emsp; + `apiKey.test.ts`: Test SHA-256 hash, constant-time comparison, reject missing/wrong key → 401, no plaintext key logging <br>&emsp; + `apiRoutes.test.ts`: Test 400 Bad Request, public routes require no key, origin secret header → reject in production mode <br>&emsp; + `apiV1Routes.test.ts`: Test all `/api/v1/*` public routes + admin session/CSRF flow <br>&emsp; + `rssClient.test.ts`: Verify XML parser disables DTD & External Entity resolution (XXE prevention) <br>&emsp; + `dedupe.test.ts`: Test canonical URL hash & title hash, block duplicate URL collection <br>&emsp; + `localPayloads.test.ts`: Test state transitions & retry logic (`CONTENT_FAILED`/`SUMMARY_FAILED` → reset; `SUMMARIZED` → 409; exceeds `MAX_RETRY_COUNT` → 409) <br>&emsp; + Build `CloudBrief_API_Tests.postman_collection.json` with all endpoints and placeholders `{{API_KEY}}`, `{{CSRF_TOKEN}}` → **51/51 tests pass** | 07/02/2026 | 07/02/2026     
| 6   | <br>&emsp; + Run full test suite after team code merge → **53/53 tests pass** <br>&emsp; + Security Audit: confirm `.env`/`cdk.context.json` in `.gitignore`, no plaintext API key in responses/logs <br>&emsp; + Verify safe-fetch SSRF protection: IP pinning after DNS resolve, block redirect > 3, block internal/IMDS IPs `169.254.169.254` <br>&emsp; + Verify Dashboard XSS protection: render summary via text encoding, not raw `innerHTML` <br>&emsp; + Verify Origin Secret Header rejects unauthorized requests in production mode <br>&emsp; + Update `docs/api.md` to match 100% of implemented `/api/v1` routes, isolate deployed-only cases | 07/03/2026 | 07/03/2026     


### Week 11 Achievements:

* Gained a solid understanding of the CloudBrief system architecture on AWS:
  * EC2 (ARM64 `t4g.small`) running API server + worker processes
  * Amazon DynamoDB for article storage and dedupe records
  * Amazon S3 for clean `.txt` content files and static frontend
  * Amazon SQS as intermediary queue between workers
  * Amazon Bedrock Nova Lite for AI summarization
  * CloudFront as the sole CDN and reverse proxy

* Wrote and operated an automated test suite including:
  * Unit tests: `apiKey`, `apiRoutes`, `apiV1Routes`, `rssClient`, `dedupe`
  * Integration tests: `localPayloads` (state transitions & retry logic)
  * All tests run **locally** without requiring actual AWS deployment

* Built a complete Postman Collection for the demo session:
  * Covers all public routes and admin routes
  * Uses placeholders `{{API_KEY}}`, `{{CSRF_TOKEN}}` (no real secrets committed)
  * Clearly annotated deployed-only cases

* Performed a Security Audit and verified the system is secure against:
  * SSRF (safe-fetch with IP pinning, blocking IMDS `169.254.169.254`)
  * XXE (DTD and External Entity disabled in the RSS parser)
  * XSS (Dashboard uses text encoding, not raw `innerHTML`)
  * API key leakage in responses, logs, or frontend assets
  * Direct EC2 bypass via Origin Secret Header enforcement

* Updated `docs/api.md` to match 100% of the implemented `/api/v1` routes.
