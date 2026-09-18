# Manuscript quality and scientific-consistency audit

## Document checks

- Abstract length: **250 words** by whitespace count.
- Abstract allocation: approximately **25% problem/challenge, 49% method, 26% results**.
- Compiled length: **42 pages** in Elsevier preprint format.
- Included figure references: **35**; missing figure files: **0**.
- Main figure assets bundled: **16 PDF files**.
- Appendix figure assets bundled: **37 PDF files**.
- Cited BibTeX keys: **34**; unresolved BibTeX keys: **0**.
- Final LaTeX pass: no undefined citations/references and no overfull boxes.
- No reviewer/editor-response language appears in the manuscript source.

## Method consistency

- The manuscript describes the **frozen H-CSMO guarded multi-profile search**, not the obsolete fuzzy/Spider-Monkey formulation of the earlier draft.
- The decision vector is joint node placement, time shift, and five-state DVFS (`3N`).
- Migration time/energy/emissions, sleep/wake states, PUE, deep-off floor, and two-layer energy/carbon accounting match the frozen evaluator.
- The deadline repair is described as a **shared evaluator operation** available to all methods.
- H-CSMO uses exact objective-call budgets, with 20 calls reserved for legacy/tail operations and the remainder assigned to base search.
- No global convergence theorem is claimed; only feasibility, call-accounting, complexity, and protected-selection properties are stated.

## Result consistency checks

- Representative overall rank leader: **hcsmo_v6d (1.98)**.
- SLA overall rank leader: **nsga_ii (2.30)**; H-CSMO is **2.64**.
- H-CSMO hypervolume rank-1 scenarios: **24/24**.
- All 60/90-task representative cells are within the 1% per-metric envelope: **True**.
- Holm-significant H-CSMO advantages over ECO-PSO, TM-MOAOA, and PPO on all five SLA metrics: **True**.
- Deadline miss and tardiness are reported from the official final-suite artifacts; the paper does not substitute older draft values.
- Runtime, migration overhead, ablation behavior, and sparse-regime exceptions remain visible in the Results/Discussion rather than being removed.

## Writing audit

- The Introduction follows problem -> application context -> technical challenges -> prior directions -> gap -> proposed solution -> accounting/evaluation design -> contributions.
- Contribution bullets describe methodological contributions only; they do not advertise numerical results.
- Related Work is organized by technical direction and discusses named methods/authors before positioning the proposed approach.
- Equations define task, node, network, power, carbon, accounting, objective, profile, pool-size, utility, and guard notation before use.
- Results emphasize the strongest reproducible evidence: representative average rank, all-scenario hypervolume, workload-level statistics, and best average SLA makespan rank.
- Claims of universal superiority, universal double-digit energy gains, or blind-confirmation success are absent.

## Submission readiness assessment

The source, references, figures, tables, and compiled PDF are internally consistent and suitable for a full manuscript revision. The article is deliberately stronger in presentation than the earlier draft while preserving the workload-level evidence needed to withstand a strict technical review. Hardware-backed validation and exact third-party source-code reproduction of adapted baselines remain outside the experimental scope and are stated as scope boundaries rather than hidden assumptions.
