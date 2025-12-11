# ML Model to Aid Quick Revision Using PYQs

## Problem Summary
Learning analytics is the domain selected for this project. The target is to build an ML model that facilitates students to prepare for exams during time constraints to ensure that their revision plan is efficient and strategic.

Generally, many candidates accelerate their pace of studying for upcoming examinations and hence experience difficulty navigating the most important topics. With enough time and effort, it is easy to recognize patterns and key topics necessary to score well on tests. But during tight schedules, candidates are less likely to review and analyze past question papers. Due to the urgency of the situation, they prefer studying materials that are quickly accessible, irrespective of the weightage of topics.

Therefore, the ML model aims to skim through past question papers and pinpoint questions that are frequently tested. This model is especially designed for time-sensitive circumstances and aims to help students be aware of the most crucial areas to focus on, supporting efficient learning and rapid revision.

## Motivation
Not knowing what to study as exam season gets closer is quite a common issue faced by many students. While consistent preparation throughout the academic term is ideal, inevitable real-world constraints often prevent this. Consequently, students may experience stress and uncertainty when attempting to revise large volumes of material in a limited time.

This project addresses this challenge by developing an ML-based tool that identifies the most frequently tested topics from past question papers. By highlighting high-priority areas, the model supports more efficient and targeted revision, reducing cognitive load and helping students make strategic decisions about their study efforts. The tool has the potential to improve learning outcomes by enabling focused revision in time-sensitive situations and contributes to the broader field of learning analytics by leveraging historical assessment data.

## Input Data Description
The model will accept historical examination data in both textual and image formats. PDFs or scanned question papers must first be converted into readable text or images, allowing the model to process the content effectively.

The expected input includes prior question papers with essential metadata, such as subject and year of the exam. The model will analyze the textual and visual content of questions to identify patterns and frequently tested topics.

## Expected Output
The model is designed to generate a concise list of high-priority topics as the output, allowing students to focus their revision effectively. The model does not hardcode subject knowledge. It is designed to only analyze patterns in the input question papers. The output is generalizable, so it can work for any subject where past question papers are available.

For example, for a general subject, the output might include 5–10 topics identified as most frequently assessed in past papers.

## Constraints & Considerations
Several limitations should be considered when using this model:

1. **Data Availability:** The model requires access to a minimum number of previous question papers to generate meaningful results. Limited or incomplete historical data may reduce accuracy.
2. **Pattern Dependency:** The model identifies frequently tested topics based on historical patterns. Unusual, novel, or recently introduced topics may not be captured.
3. **Examination Variability:** Changes in syllabus, exam format, or assessment strategy may affect the relevance of the model’s recommendations.
4. **Scope Limitations:** Certain exams, such as adaptive tests, confidential test banks, creative practical assessments, or current-affairs-based evaluations, may not benefit substantially from historical pattern analysis.

These considerations highlight that the tool is intended to supplement, not replace, comprehensive study and preparation.
