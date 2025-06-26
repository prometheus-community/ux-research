# Key Findings
## Stakeholder Interviews
We spoke to 6 stakeholders—3 from each project:

**Prometheus stakeholders:**
1. [Julius Volz](https://github.com/juliusv) - Prometheus Co-founder
2. [Beorn Rabestein](https://github.com/beorn7) - Prometheus long-time maintainer
3. [Richard Hartmann](https://github.com/RichiH) - OpenMetrics co-founder and Prometheus maintainer.

**OpenTelemetry stakeholders:**
1. [Juraci Paixão](https://github.com/jpkrohling) - OpenTelemetry Governance Committee member
2. [Josh Suereth](https://github.com/jsuereth) - OpenTelemetry Technical Committee member
3. [Austin Parker](https://github.com/austinlparker) - OpenTelemetry Governance Committee member and co-founder.

Here are insights from our conversations with the stakeholders:
- The Prometheus and OpenTelemetry communities hadn't always communicated well and that prevented them from collaborating early on.
- Much of the interoperability issues that exist now stem from the different philosophical and technical foundations on which each of the projects is built. 
> "If we think about exploratory situations or use cases, then we can justify a lot of the design decisions behind OpenTelemetry. And if we think about metrics and scaling, monitoring, for huge infra, then the design decisions for Prometheus are justified as well. So both have very good arguments." - Juraci Paixão

> “I think one of the biggest (interoperability issue) is the difference between push and pull.” - Julius Volz
- There’s a shared recognition of the importance of putting user needs first, even while maintaining some non-negotiables (like Prometheus keeping its pull model and not alienating existing users).

> [!NOTE]
> One key takeaway from the interviews was realizing that the current interoperability problems are not failures, but natural consequences of different communities solving different problems at different times. And it’s good to see both projects are working together now to make user experience better.

## User Interviews Insights
We interviewed 7 end users and they all shared incredibly helpful insights.
- The most prominent pain point users shared was the **complexity of performing joins** with the current integration.
- Regarding mental models, many users (both interviewees and survey respondents) don’t distinguish between resource attributes and Prometheus labels. They tend to think of them as the same thing.
> "I would expect resource attributes as a rule to be treated exactly the same way as the attributes attached to the tracer, the metric... I wouldn't draw a boundary between them. I think Prometheus does at the moment." - Participant 1
- As for workarounds, some users promote selected resource attributes to labels, others handle the conversion at the OpenTelemetry level to avoid dealing with it in Prometheus, and a few convert all attributes, though usually only when the number of attributes is small.

## Survey Insights
We received 134 responses in total, with 61 from our target group — people who use both OTel and Prometheus together.
Here are the key insights:
- Users don't conceptualize resource attributes as different from regular labels. 43% of respondents say they expect resource attributes to be represented "as labels" in Prometheus
- Complex join syntax is a big barrier to adoption, with 73% of respondents reporting the use of joins as challenging
- Manual attribute promotion creates operational overhead that scales poorly with team size and complexity
- 78% of respondents find documentation gaps a challenge in their use of resource attributes  

## What We Didn’t Expect to Learn (But Did)
We began this research to understand user pain points with resource attribute handling, but uncovered some unexpected and important insights. One of the most surprising was the existence of [OpenTelemetry’s telescoping feature](https://github.com/open-telemetry/opentelemetry-specification/tree/main/specification/resource#telescoping), which allows users to selectively retain or drop resource attributes based on relevance, helping to manage high-cardinality data. Despite its usefulness, many users and even some members of the Prometheus community seem unaware of it. This lack of awareness contributed to the adoption of the "join" pattern, which has since proven to be problematic.
This highlights a broader issue: documentation and education gaps are a major barrier. In our survey, 78% of respondents cited documentation gaps as a challenge.

Another key realization is that earlier integration decisions, like the reliance on joins, were made without a full understanding of each tool’s capabilities, an unavoidable consequence of the lack of early collaboration and communication between the Prometheus and OpenTelemetry communities.

## Future Blogs & Publications
We plan to share these findings and insights through blog posts on several platforms to reach the broader observability community:
- Grafana Blog
- OpenTelemetry Blog
- Cloud Native Computing Foundation (CNCF) Blog
