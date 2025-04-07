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
