# Lexi (Lan) Xiao

**Data science and analytics for operational decisions**

I work on questions of demand and resource allocation: where people go, how usage changes, and what the data can support. My public projects include spatial modeling in R and, more recently, Python tools for LLM-assisted workflows.

## Current work: AI-assisted workflows

[Resume Match Tailor](https://github.com/keeea/resume-match-tailor) is my personal Python/Copilot project for comparing resume versions against a job description and producing DOCX/PDF output.

The design separates LLM judgment from deterministic controls. Copilot selects and writes; Python checks source references, enforces workflow order, and blocks downstream steps when validated inputs change. Regression tests cover those failure paths separately from the quality of the generated wording, which still needs review.

[Workflow implementation](https://github.com/keeea/resume-match-tailor/blob/main/resume-workflow/scripts/resume_workflow/workflow.py) | [Failure-path tests](https://github.com/keeea/resume-match-tailor/blob/main/resume-workflow/tests/test_public_gates.py) | [Demo](https://github.com/keeea/resume-match-tailor#try-it-without-sharing-your-resume)

## Selected analytical work

### [Philadelphia parks: modeling demand for recreation](https://github.com/keeea/Huff_Model_for_Parks)

*2022 | Team MUSA practicum | R*

How might changes in recreation programming affect which parks people visit? Our team combined program and aggregated mobility data in a Huff spatial-choice model to explore that question.

My contributions included extending the R model to handle multiple attractiveness factors, implementing district-held-out cross-validation, and mapping prediction errors. Looking at errors geographically matters when the intended decisions concern individual facilities, not just a citywide average. The model supports scenario exploration; it does not establish that adding programs causes visits to increase.

[Model code](https://github.com/keeea/Huff_Model_for_Parks/blob/main/huffModelScripts.R) | [My evaluation contribution](https://github.com/keeea/Huff_Model_for_Parks/commit/d1aa7d0c9976449a9a436afbbf598771c6f893dd) | [Team report](https://github.com/keeea/Huff_Model_for_Parks/blob/main/PPPR_Final.Rmd)

### [San Francisco parking: estimating demand before changing prices](https://github.com/keeea/Parking-Demand-in-SF)

*2021 | Co-authored analysis | R, tidyverse, sf*

I co-authored an hourly parking-demand study using public meter records and neighborhood features. We compared OLS and Poisson models, trained on four weeks and evaluated on the following two, and examined errors by location.

We also normalized errors by meter count to compare locations with different parking capacity. The deliverables were an analysis report, maps, and pricing-interface wireframes, rather than a deployed pricing system.

[Analysis and code](https://github.com/keeea/Parking-Demand-in-SF/blob/main/Final_Report.Rmd) | [Interface concept](https://github.com/keeea/Parking-Demand-in-SF/blob/main/pics/wireframe2.png)

