<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/profile-banner-dark.png">
  <img alt="Business analyst turned data &amp; AI engineer" src="assets/profile-banner-light.png">
</picture>

The analyst half decides what is worth measuring. The engineer half builds the thing
that measures it — governed Databricks systems whose numbers are published *and
enforced*, including the ones that came out badly.

[**Technical portfolio →**](https://github.com/soulipaco/technical-portfolio) ·
[LinkedIn](https://www.linkedin.com/in/onur-uslu-10621167/)

---

## Currently

Governed text processing on Databricks. The question I keep coming back to: a table can
have clean schemas, lineage and access control while its `description` and `work_notes`
columns still carry names, emails and phone numbers.
**[pii-reduction](https://github.com/soulipaco/pii-reduction)** is my answer to it,
released as
[`v0.1.0`](https://github.com/soulipaco/pii-reduction/releases/tag/v0.1.0).

---

## Selected work

### [pii-reduction](https://github.com/soulipaco/pii-reduction)

> Structure-aware, multilingual PII reduction for Databricks
> · released `v0.1.0` · Python · Presidio + spaCy

Reduces PII inside free-text columns an operator names. A ticket id survives, a
timestamp and a speaker label survive; the name and the email do not. English, German
and Greek. **Every published number is a regression gate** — 56 of them, across three
corpora and both provider chains — so no figure in the documentation can move without a
test failing.

<table>
<tr>
<td width="210"><b>Executed</b></td>
<td>driver-path parity on a real Azure Databricks workspace; the service hosted as a Databricks App and driven over HTTPS</td>
</tr>
<tr>
<td><b>Not executed — and it says so</b></td>
<td>the distributed <code>mapInPandas</code> path is shipped and has never run; <code>ADDRESS</code> is in the taxonomy and <i>nothing detects it</i>; Greek PERSON recall is published as <code>0.500</code> rather than rounded up</td>
</tr>
<tr>
<td><b>Not claimed</b></td>
<td>it is not an estate scanner, and it promises no compliance outcome and no guaranteed anonymization</td>
</tr>
</table>

**Inspect** ·
[what was actually executed](https://github.com/soulipaco/pii-reduction/blob/main/docs/22_EVIDENCE.md) ·
[36 decision records](https://github.com/soulipaco/pii-reduction/blob/main/docs/adr/README.md) ·
[the measured baseline](https://github.com/soulipaco/pii-reduction/blob/main/docs/14_IMPLEMENTATION_PLAN.md) ·
[providers and their limits](https://github.com/soulipaco/pii-reduction/blob/main/docs/15_PROVIDERS.md)

### [contact-center-new-hire-intelligence](https://github.com/soulipaco/contact-center-new-hire-intelligence)

> Released Databricks accelerator · `v1.0.0`
> · analytics engineering · forecasting · AI/BI · Genie

Answers an operating question rather than a modelling one: when is a new-hire cohort
becoming production-ready, and what evidence supports the decision? Four governed source
tables become learning curves, volume-aware diagnostics, forecasts, process-control
views, an AI/BI dashboard, a Genie space and an optional evidence-grounded action
workflow. Release quality gates run in CI.

**Inspect** ·
[validation record](https://github.com/soulipaco/contact-center-new-hire-intelligence/blob/main/docs/validation_results.md) ·
[architecture](https://github.com/soulipaco/contact-center-new-hire-intelligence/blob/main/docs/architecture.md)

### [structure-aware-rag-databricks](https://github.com/soulipaco/structure-aware-rag-databricks)

> Released reference · `v0.1.0`
> · governed retrieval · retrieval evaluation

Built around one testable claim: fixed-window retrieval loses document structure and
evidence relationships. It preserves the hierarchy and expands exact one-hop CFR
references as separately citable evidence, against a date-pinned public eCFR corpus with
a committed evaluation set and live Databricks evidence.

**Inspect** ·
[evaluation design](https://github.com/soulipaco/structure-aware-rag-databricks/blob/main/docs/evaluation.md) ·
[retrieval design](https://github.com/soulipaco/structure-aware-rag-databricks/blob/main/docs/retrieval.md)

---

## Also in the portfolio

<table>
<tr>
<td width="250"><a href="https://github.com/soulipaco/prophet-forecasting-mlops"><b>prophet-forecasting-mlops</b></a></td>
<td>A compact, reproducible batch-forecasting reference. Forecasting behaviour stays in testable Python; Databricks-specific code is confined to delivery, tracking and persistence. A seeded synthetic source makes the contracts reviewable without private data — and the recorded run counts are execution and contract checks, not accuracy claims.</td>
</tr>
<tr>
<td><a href="https://github.com/soulipaco/databricks-genie-deployment-kit"><b>databricks-genie-deployment-kit</b></a></td>
<td>Semantic analytics managed as code: room configuration, semantic metadata, SQL examples, benchmark questions, deployment scripts and operating playbooks as reviewable assets, with a public-data Olist example. Durable repository-native dashboard evidence is still pending, because the published dashboard is not anonymously accessible.</td>
</tr>
<tr>
<td><a href="https://github.com/soulipaco/speechanalytics-databricks-pipeline"><b>speechanalytics-databricks-pipeline</b></a></td>
<td>A 16-stage contract-first speech-analytics design with per-call failure isolation and guards against raw transcript text reaching analytical outputs. <b>No recorded successful Databricks pipeline execution</b>, so it stays labelled a prototype.</td>
</tr>
</table>

---

## How I try to make the work checkable

- **Gates before claims.** A published number is enforced by a regression test, not
  restated from a notebook run nobody can repeat.
- **Evaluation kept out of the pipeline.** Ground truth comes from a generation
  manifest, so it is derived rather than reverse-engineered after the fact.
- **Reproducibility as the default.** Seeded synthetic data, pinned upstream revisions,
  locked environments, public-safe fixtures, CI on every push.
- **Limitations written down.** Each repository states what has *not* been executed and
  what it does not claim. In someone else's work, that is the list I read first.

## Earlier work

Three learning-stage repositories stay public because they show how the work developed,
not because they stand beside the systems above — an early Spark ML notebook comparing
[loan-default classification approaches](https://github.com/soulipaco/Spark-Machine-Learning-Model-Comparison),
and two absenteeism studies covering
[feature engineering and workforce modelling](https://github.com/soulipaco/Absenteeism-Dept-ML-Journey)
and [model selection across departments](https://github.com/soulipaco/Absenteeism-Model-Testing-ML-Journey).
They have notebook outputs and written findings; they do not have the reproducible
environments, tests, CI, deployment boundaries or public validation data the newer work
does.

---

[**Technical portfolio**](https://github.com/soulipaco/technical-portfolio) — the full
map, with case studies and where to inspect each proof ·
[**LinkedIn**](https://www.linkedin.com/in/onur-uslu-10621167/)
