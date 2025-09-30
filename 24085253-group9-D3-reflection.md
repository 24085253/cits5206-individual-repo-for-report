# Professional Reflection Report

## Cover Block
- **Name**: Chenglin HOU | **Student ID**: 24085253 | **Group**: 9 | **Deliverable Round**: D3 | **Project**: SmallGoods Competition App

---

## 1. Describes Experience

### 1.1 Technical Challenge: WebSocket Real-time Communication System Development

During the development phase, I took responsibility for implementing real-time communication functionality. This was my first time working with WebSocket technology, and I needed to learn and implement a stable real-time synchronization system within a short timeframe. My role was core developer, responsible for designing and implementing the entire WebSocket infrastructure.

The specific situation involved client requirements for real-time competition status updates, including pause/resume functionality, athlete order adjustments, and customizable rest periods. Technical constraints included supporting multiple client connections, ensuring reliable message transmission, and handling network interruption scenarios.

Our team initially considered using polling or long-polling approaches because of their lower implementation barriers, but we ultimately chose WebSocket technology for its superior real-time performance and reduced server load. During development, some team members encountered port conflict issues (macOS AirPlay occupying port 5000), which we resolved by switching to port 8000 and later standardizing on port 5000 [commit 14601ce].

**Evidence Anchors**: [Issue #49: Real-Time Competition Data Synchronization System](https://github.com/cits5206Group9/SmallGoods-Competition-app/issues/49), [commit 2661276: WebSocket implementation merge](https://github.com/cits5206Group9/SmallGoods-Competition-app/commit/2661276), [PR merge records](https://github.com/24085253/cits5206-individual-repo-for-report/blob/main/BRANCH_DEVELOPMENT_LOG.md)

I chose this example because it represents my biggest technical breakthrough in this project, evolving from complete unfamiliarity with WebSocket to independently designing and implementing a reliable real-time communication system.

### 1.2 Team Collaboration Challenge: Transitioning from Functional Grouping to Feature Slicing

In the early stages of the project, our team decided to allocate work based on frontend-backend functions, but during actual development we discovered this approach led to high interface integration costs and unclear responsibility boundaries. I actively participated in group discussions and proposed switching to a "feature page/vertical slice" work allocation approach.

This transition occurred during the week of beginning development, involving all 7 team members. My role was active discussion participant and advocate for the new allocation approach. The reason for change was that we found the original allocation caused one iteration rework and dampened team morale.

After the change, each person handled complete functional modules, including frontend interface, backend logic, and database design. This approach enabled faster end-to-end delivery and significantly reduced integration defects. My login page functionality [Issue #26: Create login page](https://github.com/cits5206Group9/SmallGoods-Competition-app/issues/26) was completed under this new allocation model.

**Evidence Anchors**: [commit dcd58ff: Login page functionality implementation](https://github.com/cits5206Group9/SmallGoods-Competition-app/commit/dcd58ff), [Team meeting records: 29/07/2025](https://otter.ai/u/CmpxxXMhvUZYj7RHWyvSIA596kw), [Work allocation discussion records in BRANCH_DEVELOPMENT_LOG.md](https://github.com/24085253/cits5206-individual-repo-for-report/blob/main/BRANCH_DEVELOPMENT_LOG.md)

This example is important because it demonstrates my initiative in team collaboration and problem-solving abilities, as well as practical application of agile development principles.

### 1.3 Client Requirements Understanding: MVP Document Creation Process

At the project's beginning, we faced the challenge of accurately understanding and meeting complex client requirements. The client wanted highly flexible software, including DSL (Domain Specific Language) support and dynamic scoring standards.

I actively participated in face-to-face client meetings, designing detailed question frameworks to analyze difficult points. In group discussions, I proposed an embedded "translator" solution to handle DSL requirements, translating our data structures into DSL formats familiar to users, reducing client migration costs.

This process spanned the initial phase of the project, involving clients, facilitators, and all team members. My role was requirements analyst and technical solution provider. The MVP document we created ultimately gained client approval, establishing a solid foundation for subsequent development.

**Evidence Anchors**: [Meeting records: 12/08/2025 client requirements discussion](https://otter.ai/u/ojQtTlA8u-9ks_n6pUtRqRDS9UA), [09/09/2025 meeting 1-1: DSL solution discussion](https://otter.ai/u/drZ3NK1jkNAQA0P8NdjTlfqMk6o), [09/09/2025 meeting 1-2: MVP confirmation](https://otter.ai/u/4bDpkmpTjq7sdFlibAME916AWdA), [Meeting recording screenshot](https://github.com/24085253/cits5206-individual-repo-for-report/blob/main/meetingrecording.jpg)

I chose this example because it reflects the transition from academic learning to practical work, and valuable experience in communicating with real clients.

## 2. Feelings and Evaluation

### 2.1 Emotional Journey

**Before the project started**, I felt both excited and anxious. The positive feeling came from finally having the opportunity to work on a complete IT project, allowing me to comprehensively apply knowledge from the previous three semesters. Negative feelings mainly involved concerns about excessive development pressure, particularly communication and coordination issues with team members.

**During the project**, my feelings experienced significant fluctuations. The positive aspect was discovering that some team members had strong capabilities, including development skills, design abilities, and comprehension skills, making me feel fortunate to work with excellent people. However, the complexity of client requirements temporarily brought down the entire team's morale, especially when facing technical challenges like real-time communication and DSL support.

**At the current stage**, the dominant emotion is satisfaction. In two face-to-face client meetings, our proposals gained approval, and I completely clarified client requirements, enabling full commitment to development. But there are also regrets, mainly about limited development time preventing thorough validation of many ideas, and GitHub usage skills remained insufficient.

### 2.2 Cause Analysis and Alternative Solution Evaluation

Pressure from technical challenges mainly stemmed from unfamiliarity with new technologies and high quality standards. The WebSocket technology learning curve was steeper than expected, but this challenge enabled rapid growth.

In team collaboration, the fundamental reason for early "functional grouping" failure was overlooking project scale and time constraints. Functional grouping suits large projects, but "feature slicing" was more effective for our short-term project.

In client communication, I discovered that proactive questioning and technical solution demonstrations were key to building trust. Compared to passively waiting for requirement clarification, proactive solution discussions better advanced project progress.

### 2.3 Results Evaluation

From a technical quality perspective, we implemented core functions required by the client, including real-time synchronization and flexible configuration. My WebSocket implementation proved stable and reliable through testing, and the login system's user experience received positive feedback.

From a team collaboration perspective, work allocation adjustments significantly improved development efficiency. We progressed from initial interface integration difficulties to later rapid end-to-end delivery, proving the correctness of our adjustments.

From a client satisfaction perspective, MVP documents and staged demonstrations all received positive feedback, proving we correctly understood client requirements.

## 3. Action Plan (SMART, Forward-looking)

Based on the above experiences and reflections, I recognize opportunities for immediate improvement in technical implementation and documentation quality.

| Action | Owner | Success Metric | Risk & Mitigation |
|---|---|---|---|
| Improve WebSocket system stability by adding automatic reconnection and error handling in the current codebase | I | Connection success rate ≥95% in local testing, reconnection within 3 seconds | Risk: Network environment complexity; Mitigation: Multi-scenario testing with comprehensive error logging |
| Document technical decisions and WebSocket implementation details in project README to help future maintainers | I | Complete technical documentation covering architecture, setup instructions, and troubleshooting guide | Risk: Time constraints; Mitigation: Focus on critical paths and common issues only |

## Authorship & Tools Disclosure
I used an AI assistant to help draft the structure and expression of this reflection report, but all factual content comes from my personal experiences and has been verified and confirmed by me.

## Appendix — Evidence Anchors
- **PRs**: #26 (login-page-dev), #49 (realtime-competition-sync)
- **Commits**: dcd58ff, 2661276, 14601ce, 1759ec1
- **Issues**: #26, #49
- **Meeting notes**:
  - 29/07/2025: https://otter.ai/u/CmpxxXMhvUZYj7RHWyvSIA596kw
  - 12/08/2025: https://otter.ai/u/ojQtTlA8u-9ks_n6pUtRqRDS9UA
  - 09/09/2025: https://otter.ai/u/drZ3NK1jkNAQA0P8NdjTlfqMk6o, https://otter.ai/u/4bDpkmpTjq7sdFlibAME916AWdA
  - **Meeting Recording Screenshot**: [meetingrecording.jpg](https://github.com/24085253/cits5206-individual-repo-for-report/blob/main/meetingrecording.jpg) (audio files too large to upload, screenshot provided as evidence)
- **Development Documentation**: BRANCH_DEVELOPMENT_LOG.md (uploaded to personal repo)

---