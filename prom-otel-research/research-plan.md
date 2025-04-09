## Research Overview
This UX research aims to understand how engineers use OpenTelemetry (OTel) resource attributes within Prometheus, and what improvements can enhance the OTel–Prometheus interoperability experience.
## Research Goals
Specifically, we want to:
1. Understand how engineers currently use OpenTelemetry resource attributes in conjunction with Prometheus
2. Identify pain points in the current integration between these systems
3. Discover user expectations for how resource attributes should be represented in Prometheus
## Research Questions
### Goal 1: Current Usage
- How do users conceptualize the relationship between resource attributes and labels?
- What mental model do users have when querying metrics that originated from OpenTelemetry?
- How do engineers currently map OpenTelemetry resource attributes to Prometheus labels?
- What workarounds do they currently use to bridge the gap between these systems?
### Goal 2: Pain Points in Current Integration
- Where do users experience the most friction when working with OpenTelemetry-sourced metrics in Prometheus?
- What specific tasks become difficult due to differences in metadata models?
### Goal 3: User Expectations
- What visualization and query patterns do users expect when working with resource attributes?
- How do users expect to filter and group metrics based on resource attributes?
### Feature Priorities:
- What improvements would provide the most value to users working with both systems?
- Which resource attribute use cases are most important to support natively?
## Research Methodology
### User Interviews (Qualitative)
- Conduct 30-minute semi-structured interviews with (X no. of) engineers who use both systems
- Focus on understanding their current workflows, pain points, and mental models
- Have them walk through specific tasks while thinking aloud (nice-to-have)
### Survey (Quantitative)
- Distribute a broader survey to gather data from a larger pool of users (aim for 50+ responses)
- Include questions about tool usage patterns, frequency of certain tasks, and prioritization of potential improvements
- Use Likert scales to measure satisfaction with current integration options
### Why This Research Methodology?
The decision to use interviews and surveys makes sense given what we're trying to understand. Interviews will provide deeper insights into how engineers actually work with OpenTelemetry resource attributes in Prometheus. Meanwhile, surveys (which may run alongside the interviews) will help validate whether the patterns we observe in interviews hold true across a broader range of teams and organizations.

I reviewed the [OTel End-User SIG survey](https://github.com/open-telemetry/sig-end-user/tree/main/end-user-surveys/otel-prom-interoperability) to see if we could use their findings instead of running our own survey. I noticed some overlap. However, their survey focused more broadly on OpenTelemetry and Prometheus interoperability. In contrast, our research is specifically centered on resource attributes, meaning our survey questions will need to be different.
## Target Participants
- Engineers or practitioners with hands-on experience using both Prometheus and OpenTelemetry.
- Roles may include:
  - Site Reliability Engineers (SREs)
  - DevOps Engineers
  - Platform Engineers
  - Observability Engineers
  - Backend Developers
- Working in environments where observability and monitoring are part of their day-to-day workflow.
- Experience with configuring, maintaining, or querying metrics in Prometheus.
- Familiarity with OTLP (OpenTelemetry Protocol) and how resource attributes are set or used.
## Timeline
The full project schedule is documented in this [Google Doc](https://docs.google.com/document/d/133oj-hsj6t2Hs2Yt6zpkihdbnucKeeNdF4XGXkDbrNs/edit?tab=t.hy4j88dpzfl9).

