# QA Pre‑Production

## Journey Step Focus
* How do we verify that the system behaves as expected in a production‑like environment?  
* How do we expose hidden issues that only surface under realistic load, data volume, and network conditions?  
* How do we ensure all integrations (third‑party services, APIs, infra components) are stable before go‑live?  
* How do we quantify risk and decide whether the build is ready for production deployment?

## Actions
1. Deploy the candidate release into a **pre‑production cluster** that mirrors production topology (same K8s/ECS nodes, databases, secrets, feature flags).  
2. Seed the environment with **synthetic or anonymised production data** to match traffic patterns and volume.  
3. Execute **end‑to‑end integration tests**, performance benchmarks, and security scans using automated pipelines (Jenkins/ArgoCD).  
4. Run **chaos experiments** (latency injection, service shutdowns) to validate resilience under failure conditions.  
5. Collect telemetry via **Prometheus/Grafana, Loki, Tempo**; analyze metrics for anomalies or performance regressions.  
6. Capture any failures in the defect tracking system, triage them with severity and impact, and re‑run tests after fixes.  
7. Once all checks pass and risk thresholds are met, generate a **release readiness report** for stakeholders.

## Challenges
* **Data fidelity vs privacy** – balancing realistic data usage with GDPR/PII constraints.  
* **Environment parity** – maintaining identical networking, scaling, and monitoring setups without inflating costs.  
* **Test coverage depth** – ensuring tests hit all critical paths while remaining fast enough to fit in CI pipelines.  
* **Chaos engineering risk** – avoiding accidental disruptions to shared pre‑production resources.  
* **Metric interpretation** – distinguishing normal noise from genuine regressions requires expert tuning.

## Interactions
* **Release Manager / DevOps Lead**: orchestrate the deployment and ensure rollback paths are ready.  
* **Platform Engineers**: maintain the pre‑production infrastructure, including networking, secrets, and observability stack.  
* **Security Team**: perform vulnerability scans and compliance checks in the pre‑prod environment.  
* **Performance Engineer**: design load tests, interpret metrics, and recommend capacity adjustments.  
* **QA Lead**: oversee test execution, defect management, and readiness reporting.

## Touchpoints
* ***Kubernetes / ECS** – host the isolated pre‑production cluster.  
* ***CI/CD Pipeline (GitLab CI/GitHub Actions)** – trigger deployment, testing, and report generation.  
* ***Prometheus & Grafana** – monitor latency, error rates, resource usage during tests.  
* ***Loki & Tempo** – aggregate logs and traces for root‑cause analysis.  
* ***Chaos Engineering Tool (Gremlin/Argo Rollouts)** – inject failures to test resilience.  
* ***Jira / Azure DevOps** – track defects, test results, and release readiness.  
* ***Slack / Teams** – alert teams of critical failures or rollbacks.

## Feeling
* 😌 **Confident** – when metrics confirm the system meets performance and reliability targets.  
* ⚠️ **Anxious** – if a regression appears late in testing or data volume spikes unexpectedly.  
* 🤝 **Collaborative** – when cross‑functional teams quickly resolve issues discovered during pre‑prod runs.  
* 🚀 **Empowered** – after a smooth readiness report and stakeholder sign‑off.

## Opportunities
1. **Automate synthetic data generation** (e.g., Mockaroo, DataGenie) to keep the pre‑prod environment fresh without manual seeding.  
2. **Introduce automated rollback policies** that trigger if key metrics deviate beyond thresholds during testing.  
3. **Implement predictive anomaly detection** on telemetry to flag potential regressions before tests finish.  
4. **Use canary deployment patterns** in pre‑prod to surface edge‑case failures earlier and reduce risk.  
5. **Integrate security scanning into the CI pipeline** so that vulnerabilities are caught before they reach pre‑prod.  
6. **Create reusable performance test harnesses** for common traffic scenarios, reducing duplication across releases.  
7. **Adopt a “Shift‑Left” mindset** by moving pre‑production tests earlier in the cycle (e.g., during feature freeze).  
8. **Leverage AI to prioritize test cases** based on code churn and historical failure rates.

## Potential for AI
* **AI‑driven load profile generation** – models predict realistic traffic patterns from production logs and auto‑generate corresponding synthetic loads.  
* **Predictive anomaly detection** – machine learning flags subtle deviations in metrics before they become critical failures.  
* **Intelligent test case selection** – algorithms choose the most impactful tests to run based on recent code changes and past outcomes.  
* **Automated root‑cause analysis** – NLP summarises logs, traces, and telemetry to suggest likely sources of failures.  
* **AI‑guided capacity planning** – models forecast resource needs for upcoming releases, optimizing pre‑prod scaling.
