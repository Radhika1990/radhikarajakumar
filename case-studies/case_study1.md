**3\. Case study: Improved metrics for continuous improvement:**

**Reflection for team to know their sprint performance, Qualitative and Quantitative metrics:**

**Context:**

In our Agile development process, defects are not consistently recorded, and defect metrics are not visible to the team. This lack of tracking prevents us from identifying quality trends, addressing recurring issues, and improving sprint performance. As a result, decision-making during retrospectives and planning is based on incomplete data, impacting overall product quality and team efficiency.

**Action:**

- Ensure defects are tagged as Bugs in Jira
- Made the App Server environment field in Jira as mandatory to ensure the bug reported environment is recorded correctly to separate UAT and Production bugs.
- Created customized JQL filters to filter out prod escaped defects:

Eg:

Project ="Test_Project" AND component =’XYZ’ AND type in (bug) and createddate >'2024/01/01' and "AppServer Environment\[Select List (multiple choices)\]" IN ("PROD-DEPT (Production - Internal)","PROD-INET (Production - External)","PROD-PUB (Production - External - Public)" ) order by createdDate desc

- Created two dimensional dashboards using the filter to report to team:

- Final output used in retrospectives :

**Sample Two-Dimensional Jira Dashboard - Escaped Defects**

This document represents a sample Jira dashboard widget for escaped defects, using placeholder data instead of actual sprint names. The table below mimics the structure of a Two-Dimensional Filter Statistics gadget in Jira.

| Sprint | Bug | Total |
| --- | --- | --- |
| SPR-001 / 01 Jan–15 Jan | 1   | 1   |
| SPR-002 / 16 Jan–31 Jan | 2   | 2   |
| SPR-003 / 01 Feb–15 Feb | 0   | 0   |
| SPR-004 / 16 Feb–28 Feb | 3   | 3   |
| SPR-005 / 01 Mar–15 Mar | 1   | 1   |
| SPR-006 / 16 Mar–31 Mar | 1   | 1   |
| SPR-007 / 01 Apr–15 Apr | 2   | 2   |
| SPR-008 / 16 Apr–30 Apr | 1   | 1   |
| SPR-009 / 01 May–15 May | 0   | 0   |
| SPR-010 / 16 May–31 May | 3   | 3   |
| Total Unique Issues | 14  | 14  |

**How had this Benefited the team?**

Creating Jira dashboards for defect reporting gave teams real-time visibility into bugs and I have highlighted the top benefits it created for our project:

**1\. Quality Monitoring**

- **Track Bugs Over Time: Helps identify trends in defect rates across sprints.**
- **Early Detection: Spot recurring issues early and address root causes.**
- **Release Readiness: Gauge whether a product is stable enough for release.**

**2\. Process Improvement**

- **Identify Bottlenecks**: High defect counts in certain sprints may indicate issues in development or testing processes.

**Team Performance Insights**

- **Velocity vs. Quality**: Balancing speed of delivery with quality by comparing story points completed vs. defects found.
- **Accountability and Ownership**: Encourages teams to take ownership of quality, not just delivery.

**4\. Retrospective Discussions**

- **Data-Driven Retrospectives**: Use defect metrics to guide discussions on what went well and what needs improvement.
- **Actionable Feedback**: Helps teams set measurable goals for reducing defects in future sprints.

**5\. Stakeholder Communication**

- **Transparency**: Provides stakeholders with a clear view of product quality.
- **Progress Reporting**: Demonstrates improvements or regressions in quality over time.
