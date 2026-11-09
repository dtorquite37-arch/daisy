# Student Performance Prediction System – Laboratory Submission

**Name:** ______________________  **Section:** ____________  **Date:** ____________

## 1. SAD mini-analysis
| Element | Response |
|---|---|
| Problem statement | Academic risk is often noticed after poor results. The prototype explores early identification using available student indicators. |
| User | Faculty member or academic analyst. |
| Inputs | Student attributes and academic indicators (study time, absences, failures, G1, G2, etc.). |
| Process | Validate data -> preprocess -> apply trained model -> classify risk. |
| Outputs | AT RISK / NOT AT RISK label and model evaluation summary. |
| Key limitation | A model trained on one Portuguese secondary-school dataset may not generalize to another institution or population. |

## 2. Model evaluation results
Paste your own output from `python train_model.py`:

| Metric | Value |
|---|---|
| Accuracy | |
| Precision (At risk) | |
| Recall (At risk) | |
| F1-score (At risk) | |

## 3. Testing
| Test | Pass? |
|---|---|
| Run train_model.py (CSV and model files created) | ☐ |
| Run Streamlit app (dashboard loads) | ☐ |
| Upload sample CSV (predictions displayed) | ☐ |
| Upload CSV missing a required column (helpful error shown) | ☐ |
| Download results (CSV with predictions) | ☐ |
| Open GitHub repository (files and README visible) | ☐ |

## 4. Reflection
1. **Prediction target and why G3 is excluded.** The target is whether a student is at risk: 1 if final grade G3 < 10, otherwise 0. G3 is excluded from the inputs because it *is* the answer; including it would be target leakage, making the model look perfect while being useless for real early prediction.
2. **Recall for the "At risk" class.** Recall is the share of truly at-risk students that the model correctly flags. A high recall means few at-risk students are missed; a low recall means many are overlooked (false negatives), which matters because the goal is to give support to those who need it.
3. **Why performance may differ at my institution.** The data comes from two Portuguese secondary schools. Grading scales, curriculum, culture, demographics, and support systems differ elsewhere, so the patterns learned may not transfer (dataset shift). The model should be re-validated or retrained on local data.
4. **Action after an "AT RISK" prediction.** Treat it as a prompt, not a verdict: review the student's actual records, talk with the student and, where appropriate, guardians or advisers, and offer support such as tutoring or consultation. Do not use the prediction alone for grading or disciplinary decisions.

## 5. Links
- GitHub repository URL: https://github.com/YOUR-USERNAME/student-performance-prediction
- Screenshots attached: ☐ dashboard  ☐ prediction results
