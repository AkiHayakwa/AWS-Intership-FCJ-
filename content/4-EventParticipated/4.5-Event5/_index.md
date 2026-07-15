---
title: "Event 5"
date: 2026-07-11
weight: 5
chapter: false
pre: " <b> 4.5. </b> "
---

# Event Report "First Cloud AI Journey - AWS SLA, Security & Exam Roadmaps"

### Event Purpose

- Strategically guide and build a roadmap for beginners to conquer the AWS Certified Cloud Practitioner (CLF-C02) exam.
- Analyze the importance of monitoring based on end-user experience instead of relying solely on technical infrastructure.
- Introduce automated AI security solutions to optimize cost and performance compared to manual methods.
- Equip participants with a system risk management mindset and apply AWS standard models in practice.

### Speakers List

- **Nguyễn Huỳnh Sơn** - Member of AWS Student Builder Group HUFLIT, Ex Infrastructure Reliability Engineer at SPS; shared on the topic of SLA and Monitoring systems.
- **Ngo Le Tan Huy** - Speaker guiding the strategic roadmap and tips for the AWS Cloud Practitioner exam.
- **Thinh Nguyen (Nguyen Tuan Thinh)** - DevOps/DevSecOps/Cloud Engineer at Styl Solutions; shared on automated security solutions with AWS Security Agent.

### Key Highlights

#### 1. Monitoring System and Service Level Agreement (SLA)
- **Nature of SLA**: A formal agreement on the level of service between a provider and a customer. AWS is responsible for guaranteeing their services, but the actual user experience is the responsibility of the system builders.
- **Infrastructure monitoring loopholes**: A "green" infrastructure status (normal CPU, RAM) does not mean users have a good experience. For example: A health check endpoint (`/health`) may work fine, but the actual login flow (`/login`) might fail due to a database connection error.
- **Monitoring Pyramid Model**:
  - **Bottom tier (Infrastructure/Cloud Services)**: CPU, Memory, EC2, RDS to diagnose root causes.
  - **Top tier (User Experience/Business)**: Login success rate, revenue, orders help determine the actual impact level.
- **Risk Management Cycle**: Risk identification $\rightarrow$ Signal monitoring (metrics, logs, alarms) $\rightarrow$ Automated feedback via SNS/Slack $\rightarrow$ System improvement.

#### 2. Strategy to conquer AWS Cloud Practitioner (CLF-C02)
- **Exam Structure**: 65 multiple-choice questions (single or multiple answers), 90 minutes (non-native English speakers get 30 extra minutes), passing score 700/1000. Certificate is valid for 3 years.
- **4 Key Knowledge Domains**:
  - **Cloud Concepts (24%)**: Focus on digital transformation mindset, 6 benefits of Cloud, Well-Architected framework, and CAF.
  - **Security and Compliance (30%)**: Shared responsibility model (Security OF vs IN the cloud), IAM, security groups (Security Groups/NACLs), AWS Artifact.
  - **Cloud Technology and Services (34%)**: Understand use cases through service names (Compute, Storage, Database, Networking).
  - **Billing, Pricing, and Support (12%)**: EC2 pricing models, cost management tools (Cost Explorer, Budgets), and support plans.
- **Effective Study Methods**:
  - **Keyword Mapping Mindset**: Associate each service with 1-2 core keywords (e.g., "Decouple" $\rightarrow$ SQS).
  - **Error Analysis**: When doing mock exams, clarify why other options are wrong to avoid exam traps.
  - **Free Tier Practice**: Directly interact with basic services for easier visualization.

#### 3. Optimizing Web Application Security with AWS Security Agent
- **Bottlenecks of Traditional Pentest**: Manual testing often takes weeks, is expensive ($5k - $20k), and results vary depending on the expert's skill.
- **Automated AI Solution (Frontier Agent)**: Powered by Amazon Bedrock, capable of autonomously planning and verifying vulnerabilities through actual exploitation rather than just giving theoretical warnings.
- **Comprehensive Coverage**:
  - **Design Review**: Check Markdown documents or Terraform code right from the design phase according to PCI DSS, NIST CSF standards.
  - **Code Review**: Automatically integrate into Pull Requests on GitHub/GitLab to scan for malware, exposed secrets, and suggest direct patch fixes.
  - **Automated Pentesting**: Perform multi-step chain attacks (IDOR $\rightarrow$ XSS) like a real user.
- **Core Limitations**: Blocked by complex authentication systems (MFA, Biometrics, mTLS) and struggles to detect business logic frauds.

---

### What I Learned

#### Design & Management Mindset
- A stable infrastructure service is only a prerequisite; the sufficient condition for evaluating a good system is the satisfaction and seamless experience of the end user.
- Information security needs to be integrated early (Shift-left security) right from the architecture design phase through automated scanning tools to minimize future remediation costs.

#### Technical & Tools
- Learned how to set up Custom metrics combined with CloudWatch Alarms and SNS to receive early warnings before customers even report issues.
- Mastered AWS multiple-choice exam techniques such as the elimination method for distractors and paying attention to decisive keywords (Not, Least cost, Most scalable).
- Clearly understood the task-hour based pricing model of security AI agents to balance costs against hiring personnel.

---

### Applying to Work

- **Rebuild the monitoring Dashboard system** for current projects: Add application layer and business experience metrics (Login rate, successful checkout rate) instead of just looking at CPU/RAM charts.
- **Plan to study for the AWS Certified Cloud Practitioner** certificate following the 4-domain roadmap, utilize free AWS Skill Builder resources, and practice on a Free Tier account.
- **Experiment with integrating automated source code scanning tools** into the team's CI/CD pipeline to automatically check security upon every Pull Request creation.

![First Cloud AI Journey](/images/4-EventParticipated/4.5-Event5/z8039068243577_1016755ae263c32512c060d417ef7767.jpg)

