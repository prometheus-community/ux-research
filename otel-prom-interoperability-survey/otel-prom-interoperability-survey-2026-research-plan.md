# Survey: OTel ↔ Prometheus Interoperability '26

#### Research plan

Authors: Andrej Kiripolsky, Ana Muenz, Arthur Sens

## Background

In 2024 we ran a survey about OTel and Prometheus interoperability to help inform some of the decisions communities were making to make these two projects more compatible. In 2026, new challenges are relevant for us and we have a new set of questions to ask.  

## Research questions

1. How easy is it for users to use OTel and Prometheus together?
2. How do users prefer to instrument their infrastructure and applications?

## Method

To answer these research questions, we will run a survey where we will ask people who use both Prometheus and OpenTelemetry about their experience and opinions.

We will look for participants in two ways. First, we will use the usual SIG End-user channels (LinkedIn, Mastodon, and Bluesky), as well as a website banner if possible. Also, we will be collecting responses IRL at KubeCon Europe 2026 in Amsterdam – either at Prometheus booth, OpenTelemetry table, or randomly at the venue. 

## Questionnaire

#### Conversation starter for KubeCon

Hey, do you use Prometheus and OpenTelemetry? I am doing a survey about them. Would you like to share your experience with me, please?

The survey is anonymous; data will be published in our public repo under a public domain licence. Do you want me to read you a full privacy notice, or shall we skip to the questions right away. 

#### Section 1

Do OpenTelemetry and Prometheus play nicely in your stack? OTel and Prometheus communities want to know! This survey is our way of understanding how people use our tools in the real world — and where the rough edges are. Your experience matters to us!

***Privacy notice:** The data collected in this survey will be anonymised and publicly shared in the GitHub repositories prometheus-community/ux-research and opentelemetry/sig-end-user under the ++[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)++ Universal public domain dedication. This means anyone can freely use, share, and build upon the data without restriction. By submitting this survey, you acknowledge that your anonymised responses will be made publicly available under these terms. Questions? Contact #prometheus-ux-wg or #otel-sig-end-user at CNCF Community Slack.*

#### Section 2: OpenTelemetry

1. Do you use OpenTelemetry in production for metrics? (*)
   1. Yes
   2. No

_If answer option 2 was selected, submit form._

#### Section 3: Prometheus

2. Where do you store your metrics primarily? (*)
   1. Prometheus
   2. Open-source Prometheus backend (Thanos, Cortex, Grafana Mimir)
   3. Prometheus-compatible (or PromQL compatible) backend from a vendor
   4. A backend not associated with Prometheus, not compatible with PromQL  
   5. I don’t know 
   6. Other…(type in)  

_If answer option 4, 5, or 6 was selected, submit form._

#### Section 4: Role

3. What type of team do you work on? (*)
   1. Dev
   2. DevOps
   3. Operations
   4. SRE
   5. Platform Engineering
   6. Observability
   7. Sysadmin
   8. Sales Engineering
   9. DevRel
   10. Other…(type in) 

  _If answer option 10 was selected, submit form._

#### Section 5: Infrastructure instrumentation

4. How do you instrument infrastructure metrics collection? (choose all that apply) (*)
   1. I don't collect infrastructure metrics
   2. OTel receivers
   3. Prometheus exporters
   4. Built-in /metrics endpoint (without exporter)
   5. Built-in OTLP push
   6. OpenTelemetry eBPF Instrumentation (a.k.a. OBI)
   7. I don’t know
   8. Other…(type in)

#### Section 6: Applications instrumentation

5. How do you instrument application metrics collection? (choose all that apply) (*)
   1. I don't collect application metrics
   2. OTel SDKs
   3. Prometheus SDKs
   4. OpenTelemetry eBPF Instrumentation (a.k.a. OBI)
   5. I don’t know
   6. Other…(type in)

#### Section 7: Telemetry processing

6. What do you use to process or transform metrics data before you send it to storage? (choose all that apply) (*)
   1. Nothing, it goes to storage right away
   2. Prometheus relabeling rules or record evaluations
   3. Open source OTel Collector (core, contrib)
   4. Custom-built OTel Collector built with OCB
   5. Vendor distribution of OTel Collector
   6. I don’t know
   7. Other…(type in)

#### Section 8: Ease-of-use and open feedback

7. How easy or difficult is it to use OpenTelemetry and Prometheus together? (*)
   1. Very easy
   2. Somewhat easy
   3. Neither easy nor difficult
   4. Somewhat difficult
   5. Very difficult

8. What would you like us to improve to make OpenTelemetry and Prometheus work better together? (optional)
   1. Open feedback

#### Section 9: Demographic questions 1

9. What industry do you work in? (*)
   1. Technology
   2. Retail
   3. Finance
   4. Other
   5. I am not employed right now 
   6. I am a student 

  _If answer option 5 or 6 was selected, submit form._

#### Section 10: Demographic questions 2

10. Where in its observability journey is your organization? (*)
   1. Beginner - Learning about observability / Have used monitoring tools
   2. Intermediate - Setting up an observability practice
   3. Intermediate - We are setting up an observability practice
   4. Expert - Having a well-established observability practice
   5. Expert - We have a well-established observability practice

11. How large is your organization? (*)
   1. 1-49 employees
   2. 50-99 employees
   3. 100-999 employees
   4. 1000+ employees

12. Do you work for an observability or APM (monitoring) vendor? (*)
   1. Yes
   2. No

13. Are you a Prometheus or an OpenTelemetry maintainer? (*)
   1. Yes
   2. No

#### Thank you message

## Lessons learned

1. Pilot the survey
   - We ran this survey first in person at KubeCon Europe 2026 in Amsterdam. After the first few conversations we right awat noticed that we should change the survey if we want it to make sense (Thanos and other projects are also relevant for us). And then again (Using Prometheus and OTel at the same time, doesn't necessairly mean using them together). Piloting the survey before the main run can be very useful. We should do it regularly. 

