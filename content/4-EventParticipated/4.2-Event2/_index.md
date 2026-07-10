---
title: "Event 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Summary Report: Event on June 13th

### Event Objectives

- Career orientation and sharing development journeys in the IT industry.
- Analysis of a real-world system architecture (Case study: URL Shortener) on cloud platforms.
- Deep-dive into Data Analytics and career growth path across different seniority levels.
- Comprehensive overview of the recruitment process, culture in Multi-National Corporations (MNCs), and work philosophy.
- A realistic picture of DevOps Engineer responsibilities compared to theory.

### Speakers

- **Mr. Danh Hoang Hieu Nghi** - Topic: Career journey and identifying users' actual problems.
- **Mr. Trung Kien (Leader) & Mr. Nguyen Minh Tho** - Topic: Project architecture analysis of a URL Shortener application.
- **Mr. Dat Pham** - Topic: Data Analytics and career mindset roadmap.
- **Mr. Nguyen Cuong** - Topic: Corporate culture (MNC) and the philosophy of "Doing It Right".
- **Mr. Trong H Truong (DevOps at Endava)** - Topic: What does a DevOps Engineer actually do?

---

### Key Highlights

#### Career Journey & Problem Solving (Mr. Hieu Nghi)
- **Orientation**: Sharing personal development paths in the industry.
- **Mindset**: Emphasized the vital importance of deep diving into core systems to identify user pain points, enabling technical teams to design precise and highly valuable software solutions.

#### URL Shortener Architecture (Mr. Trung Kien & Mr. Minh Tho)
- **Solving System Bottlenecks**: Defined architectural challenges under heavy web traffic and how cloud services mitigate scaling issues.
- **Three-Tier Architecture**:
    - **Frontend & Edge**: A unified combination of Amazon CloudFront, AWS WAF, and AWS Amplify.
    - **Processing (Compute & Cache)**: Amazon ECS processes hash encoding, communicating with ElastiCache (Redis).
    - **Database Layer**: Data is persisted in Amazon DynamoDB.
- **Data Flow (Cache-aside pattern)**: Client requests check ElastiCache first (cache hit immediately returns). If missing (cache miss), the system queries DynamoDB, retrieves/creates the redirect mapping, and populates the cache for future hits.
- **4 System Advantages**:
    1. Separation of concerns.
    2. Defense at the edge (security shielding via WAF & CloudFront).
    3. Pre-computation.
    4. Cache-aside model implementation.

#### Data Analytics & MNC Culture (Mr. Dat Pham & Mr. Nguyen Cuong)

##### Part 1: Data Analytics (Mr. Dat Pham)
- **Responsibilities**: Weekly reporting, root cause analysis, cross-functional communication, detailed cost/risk analysis, and business metrics tracking (e.g., conversion/order ratios).
- **Core Skills**: Critical thinking, communications, data storytelling, and a growth mindset.
- **Mindset**: Explain complex technicalities from a layman's perspective. Understand what numbers represent in the physical business world.
- **5 Levels of Professional Growth**:
    - Follower: Intern, requires hands-on instructions.
    - Learner: Understands tasks but still needs oversight.
    - Problem Solver: Autonomously handles assigned tickets.
    - System Thinker: Comprehends global system impact (e.g., how compliance/regulations impact company operations).
    - Super Star: Designs structural roadmaps, long-term strategies, and business positioning.

##### Part 2: MNC Culture & "Doing It Right" (Mr. Nguyen Cuong)
- **MNC Recruitment**: 4 stages (CV screening/phone screening -> competency test -> technical interview -> cultural fit assessment).
- **Company Culture**: The combination of "thinking style, living style, working style" shared by all company members.
- **Integration Context**: Analyzed Vietnam's economic milestones (1975-1986 isolation, 1986-1995 Doi Moi, 1997 Internet & WTO integration). Emphasized that Vietnam must aim for international compliance standards, specifically data privacy integrity.
- **"Doing It Right" Philosophy (TS. Gian Tu Trung)**:
    - Being Human: Decency (Social sphere).
    - Doing a Job: Solving real-world issues with a service mindset (Economic sphere).
    - Being a Citizen: National responsibility, contributing to country development (Political sphere).

#### DevOps in Reality (Mr. Trong H. Truong)
- **Why DevOps**: Highly reputable, good salary, great market demand. Despite AI advancements, DevOps remains critical.
- **Reality vs. Theory**: Theory covers coding, CI/CD pipelines, and Docker. In reality, responsibilities vary by scale (Startups vs. Enterprise). At startups, DevOps engineers wear many hats and handle multiple roles.
- **Tooling**: Broad knowledge from Linux, Networking, Git, languages, CI/CD to containers. However, tools change continuously.
- **DevOps Survival Mindset**:
    - Verify copy-pasted code snippets; learn from real errors.
    - Interpersonal communication is highly critical.
    - DevOps engineers are not free helpers; they need dedicated time to address critical incidents.
    - System Thinking over task-focused mindset. Maintain a clean, maintainable architecture.
    - Use AI to boost productivity, not lazy thinking.

---

### Key Takeaways

#### Design & Technical Mindset
- Mastered the Cache-aside workflow and the power of modular Separation of Concerns.
- Understood the importance of blocking malicious traffic at the outer layer (Defense at the edge) rather than letting it hit backend compute instances.
- Learned that data remains silent without "Data Storytelling". Always view metrics from the end-user's perspective.

#### Soft Skills & Career Orientation
- Promotion depends not just on coding skills but on migrating from a Problem Solver mindset to a System Thinker mindset.
- Communication is the ultimate survival skill in both Data Analytics and DevOps to bridge cross-team gaps and align goals.
- Learned to use AI as an accelerator for task execution while keeping core analytical thinking sharp.

#### Applying to Work
- **Defense at the edge**: Configured AWS WAF alongside Amazon CloudFront and AWS Amplify to secure static UI assets at the edge, blocking DDoS and Prompt Injection before hitting backend gateways.
- **Separation of Concerns**: Utilized Lambda for auto-scaled compute and DynamoDB for persistent storage, separating application tiers.
- **System Thinking**: Instead of working in silos, mapped the entire architecture flow (Route 53 -> Frontend -> API Gateway -> Lambda -> DynamoDB/Bedrock) to understand error propagation.
- **Corporate Readiness**: Adopted the "Doing It Right" philosophy to work professionally in a multinational corporate environment.

---

### Event Experience

The event on June 12th provided real-world engineering insights that are rarely detailed in academic textbooks.
- The highlights were the URL Shortener architecture case study by Mr. Kien and Mr. Tho, demonstrating how cloud computing patterns scale under massive traffic.
- Data Analytics and DevOps segments broke the idealized assumptions. I realized that communication and System Thinking determine success in any IT role. The concept of working with a "service spirit" and triết lý "Đúng việc" serves as a precious guide for my internship.

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; margin: 20px 0;">
  <img src="/images/4-Event/Event_2/1783623797240_46021865491134503_4221743142166198034_1a0e76879a07423c6925fd02f4a8fc2c.jpg" width="300" style="border-radius: 8px; object-fit: cover;" />
  <img src="/images/4-Event/Event_2/1783623797975_46021865491134503_4221743142166198034_7fcd8c22a3a332c92da7c655f5854746.jpg" width="300" style="border-radius: 8px; object-fit: cover;" />
  <img src="/images/4-Event/Event_2/1783623867924_46021865491134503_4221743142166198034_6119e334fdf1b4913017eb68520be570.jpg" width="300" style="border-radius: 8px; object-fit: cover;" />
  <img src="/images/4-Event/Event_2/1783623868997_46021865491134503_4221743142166198034_279f3d21886b1dd7d5efac9d88331006.jpg" width="300" style="border-radius: 8px; object-fit: cover;" />
  <img src="/images/4-Event/Event_2/1783623869875_46021865491134503_4221743142166198034_607908fbcdd665865ce0132831132889.jpg" width="300" style="border-radius: 8px; object-fit: cover;" />
  <img src="/images/4-Event/Event_2/1783623870476_46021865491134503_4221743142166198034_97a60690894789e08d9fab2fa5b5018f.jpg" width="300" style="border-radius: 8px; object-fit: cover;" />
</div>

> Overall, the event on June 13th offered a practical orientation, spanning scaling architectural patterns (Cache-aside, edge security shielding) to hard realities of DevOps and Data roles. The key lesson is the transition from a tool Learner to a global System Thinker. Additionally, the "Doing It Right" philosophy is vital for any engineer working in multinational structures.
