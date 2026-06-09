---
title: "Event 3"
date: 2026-06-06
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

# Summary Report: “First Cloud Journey Meetup - June 2026”

### Event Objectives

- Share knowledge about Container technology and Docker for beginners.
- Introduce advanced solutions like GraphRAG on AWS Bedrock and Neptune.
- Guide on building a Network Intrusion Detection System (NIDS) using Machine Learning.
- Share practical career path experiences from IT Helpdesk to Senior Sysadmin/Cloud Engineer.
- Explore multiplayer game connection architectures using AWS WebSockets and Godot.
- Emphasize golden rules and tools for effective teamwork.

### Speakers

- **Bao Huynh** – Junior Cloud Native Developer at Endava Vietnam & Founder ITea Lab.
- **Viet Phat** – AI Major at Swinburne University of Technology.
- **Lê Hoàng Gia Đại** – Final-year student at HUTECH, Team AWS G3.
- **Tran Trung Vinh** – System Administrator at Central Retail Group.
- **Nguyen Quoc Bao** – Speaker on Multiplayer Cloud Networking.
- **Truong Huy Phuoc** – Speaker on The Art of Effective Teamwork.

### Key Highlights

#### Docker - Containerization Technology
- **Concept:** Packages applications and their dependencies into a single package to run consistently anywhere.
- **Benefits:** High portability, consistency, resource efficiency, and rapid deployment.
- **Core Components:** Docker Images (read-only templates), Dockerfile (instructions to build images), and Docker Containers (running application instances).

#### GraphRAG with Amazon Bedrock & Neptune
- **Problem:** Traditional RAG is limited in answering queries requiring multi-hop reasoning.
- **Solution:** Use Graphs to store explicit relationships between entities, enabling LLMs to understand context more deeply.
- **Tools:** Amazon Bedrock (entity processing/embedding) and Amazon Neptune (graph storage and querying).

#### Machine Learning-based NIDS (Network Intrusion Detection System)
- **Necessity:** Traditional WAF rules are insufficient against Zero-day attacks or anomalous behaviors.
- **Mechanism:** Use Machine Learning (e.g., LightGBM algorithm) trained on real-world network data (CSE-CIC-IDS2018 dataset) to detect threats.
- **Ecosystem:** Combine AWS WAF with services like Lambda, S3, and GuardDuty to build an active security shield.

#### IT Infrastructure Career Path
- **Core Skills:** Start with troubleshooting, communication, and a continuous learning mindset at the Helpdesk.
- **Transition:** Learn Linux, Networking, and build hands-on labs to understand how systems are constructed.
- **Cloud/DevOps Mindset:** Shift from managing physical servers to Infrastructure as Code (IaC - Terraform) and automation culture (CI/CD, Docker).

#### Multiplayer Game Connectivity with AWS WebSockets
- **Architecture:** Utilize API Gateway WebSockets to maintain full-duplex, two-way connections.
- **State Management:** Combine Lambda (processing logic) and DynamoDB (storing connection IDs and match states).
- **Godot Integration:** Use the `WebSocketPeer` class to handle network events in the game loop.

### Key Takeaways

#### Design Mindset
- **Cloud-Native Mindset:** Understand elastic scaling and pay-for-value models.
- **Security-First:** Security is not just about static rules but requires the flexibility of AI/ML to adapt to new threats.
- **Teamwork Core:** A clear common goal and individual accountability are key to team performance.

#### Technical Architecture
- **Containerization vs. Virtualization:** Understand why Containers are lightweight and more optimized than traditional VMs by sharing the host OS.
- **Real-time Communication:** Differentiate when to use WebSockets (for turn-based games, chat) and when to use GameLift for games requiring high update frequencies.
- **Data Engineering for AI:** The importance of data cleaning and handling class imbalance during ML model training.

#### Career Development Strategy
- **Hands-on Experience:** Building real projects and a portfolio is more important than certificates alone.
- **Automation:** Automate repetitive tasks to focus on system design and improvement.

### Applying to Work

- **Deploy Docker:** Containerize current applications to optimize CI/CD processes and reduce infrastructure costs.
- **Upgrade Security:** Research integrating ML NIDS into the existing AWS architecture to enhance threat detection capabilities.
- **Improve Teamwork:** Use tools like Trello, Slack, or Discord to manage projects and communicate effectively following golden rules.
- **WebSocket Web Development:** Experiment with building real-time interactive features using AWS Lambda and DynamoDB.

### Event Experience

Participating in the Meetup on June 06, 2026 was a multidimensional learning journey from infrastructure, security to application development. Some highlights include:

#### Learning from Practice
- Stories about mistakes in the Sysadmin journey and the golden rule "never test in production" brought great practical value.
- Live demo sessions connecting the Godot game and observing real-time DynamoDB data helped clarify abstract concepts.

#### Pioneering Technology Updates
- Exposed to GraphRAG - a new trend that solves complex reasoning problems traditional RAG cannot.
- Understood how to combine Cloud-native power with Machine Learning to protect systems against modern attacks.

#### Community Connection
- The event created space for students, newcomers, and experts to exchange career paths "from scratch".
- Learned the importance of digital tools in driving smooth collaboration among team members.

### Lessons Learned

- Technology is only a tool; correct design thinking and persistence in hands-on practice are the keys to success.
- Modernizing applications through Docker and Serverless helps businesses accelerate time-to-market and reduce operational risks.

> Overall, the event provided a comprehensive picture of the AWS ecosystem and how technologies like AI, Containers, and WebSockets are transforming software development.
