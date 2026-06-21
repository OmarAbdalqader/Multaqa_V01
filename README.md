<div align="center">
  
# 🌐 Multaqa Platform

**A Comprehensive Academic-Professional Hub**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Click%20Here-success?style=for-the-badge&logo=google-earth)](http://multaqa.theomar.xyz/)

</div>

---

**Multaqa** is a comprehensive academic-professional platform designed to connect students with universities, companies, and non-profit organizations. It provides an integrated digital environment that simulates students' academic needs and prepares them for the labor market by balancing learning, networking, and professional development.

---

## 📋 Table of Contents
- [Technology Stack & Architecture](#️-technology-stack--architecture)
- [User Roles](#-user-roles-16-distinct-roles)
- [Core Systems](#️-core-systems-17-integrated-systems)
- [About the Developer](#-about-the-developer)

---

## 🛠️ Technology Stack & Architecture

The platform is built on a robust architecture ensuring high performance and sustainable security:

* **Backend Framework:** ASP.NET Core 8 MVC
* **Database Management:** SQL Server via Entity Framework Core
* **Real-Time Engine:** SignalR *(Powers chats, instant notifications, and live debates)*
* **Cloud Storage:** Amazon S3 *(Secure storage for files, images, and documents)*
* **Artificial Intelligence:** Groq LLM (Llama 3.3) for the Smart Virtual Interview system
* **APIs & Code Execution:** 
  * **Google Custom Search API:** Automates fetching educational resources for the Skills Gap system.
  * **Wandbox API:** Provides a secure sandbox environment for compiling and executing code in 25+ programming languages.
* **DevOps & Deployment:** Dockerized application deployed on AWS via ECR and EC2.
* **Design Patterns & Data Protection:** Implements the Soft Delete pattern (`IsDeleted`) to prevent permanent data loss, and utilizes a dedicated `ContentFacultyTargets` table for precise content targeting.

---

## 👥 User Roles (16 Distinct Roles)

The platform features an advanced Role-Based Access Control (RBAC) system supporting 16 different user types across four main sectors:

| Sector | Roles & Functions |
| :--- | :--- |
| **💼 Professional** | Company Manager, Company Editor, Event Manager, Company Ambassador |
| **🎓 Academic** | Student, Teacher, Student Organization Leader, Organization Member |
| **🏛️ Administrative** | University Manager, Faculty Manager, Platform Moderator, Content Reviewer |
| **🌐 Community** | External User, Non-Profit Representative, Advertiser |

---

## ⚙️ Core Systems (17 Integrated Systems)

### 1. University Organizations System (Teams)
A dedicated environment for managing student clubs and societies (tech, sports, cultural) within the campus.
* **Role Management:** Hierarchical permission distribution (Leader, Co-Leader, Moderator, Member).
* **Privacy & Governance:** Supports multiple visibility levels (Public, Private, Hidden) and requires university administration approval prior to activation.
* **Targeting:** Ability to publish activities aimed at specific faculties or academic departments.

### 2. Non-Profits System
A bridge connecting external mentorship institutions with students for guidance and awareness sessions.
* **Booking Workflow:** Organization Registration ➡️ Moderator Approval ➡️ Publishing Session Slots ➡️ Student Request ➡️ Assigning Representative ➡️ Automated instant chat room creation.
* **Management Tools:** Dedicated dashboard for organizations to track mentorship requests and session analytics.

### 3. Mentorship System
An advanced system allowing industry experts to provide one-on-one consultations to students.
* **Flexible Scheduling:** Customizable recurring weekly availability.
* **Communication Channels:** Supports text, audio, and video sessions (Free or Paid).
* **Automation:** Automatically generates meeting links and chat rooms once the mentor accepts the request.

### 4. Company Tasks & Opportunities
A comprehensive gateway connecting companies with student talent through two tracks:
* **A) Freelance Opportunities:**
  * Post tasks with specific financial rewards.
  * Integrated application system (CV + Cover Letter).
  * Digital contracts signed by both parties within the platform.
  * Delivery Lifecycle: Submission ➡️ Review (Accept/Edit) ➡️ Closure and mutual rating.
* **B) Coding Challenges:**
  * Integrated programming assessment environment supporting 25+ languages.
  * Advanced in-browser IDE.
  * Timed challenges with an anti-cheat system (detects tab switching and auto-disqualifies after 3 attempts).

### 5. Smart Social Feed
A custom algorithm designed to rank and display academic and professional content based on academic relevance and engagement:

```math
\text{Score} = (\text{Faculty Match} \times 3) + (\text{University Match} \times 2) + (\text{Engagement Level} \times 4) + (\text{Recency Score } [0\text{-}5])
