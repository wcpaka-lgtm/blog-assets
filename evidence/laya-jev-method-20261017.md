# Laya versus Jev: archived experiment and label audit

The experiment ran on September 21, 2026. These files were extracted and audited on October 17; they are not a new model run. All sixteen tickets are synthetic fixtures written for the experiment, not customer records.

The JSON contains the exact question definitions, input fixtures, original reference labels, model scores, rounded urgency decisions and recorded latency. The CSV exposes the same sixteen rows for inspection. The original counts are Jev 45/48 and Laya 37/48. Those are matches with the author's provisional labels, not independently validated accuracy.

At least two labels contradict the supplied urgency rubric: case 15 says “Not urgent” but has reference urgency 1, while case 16 says the team is “locked out” but has urgency 1 although the rubric assigns blocked cases 2. We preserve these original labels to make the defect visible. We do not silently relabel the experiment or claim a corrected accuracy ranking. A new evaluation needs a consistent rubric, independently checked labels and more varied held-out examples.

Laya ran locally on an i5-10400F / GTX 1080 Ti 11 GB machine. Jev was hosted behind a network endpoint; its times include the round trip from Korea. A latency ratio across these two paths is not an architecture-only speed benchmark. The first recorded Laya case includes startup effects. The accompanying article distinguishes repeated warm latency measurements from this single head-to-head pass.

Scoring: department is an exact category match, urgency is rounded to the nearest integer, and the refund probability is classified at 0.5. The raw urgency scores are retained so other thresholds can be inspected. Vendor benchmark figures are separate from this experiment.
