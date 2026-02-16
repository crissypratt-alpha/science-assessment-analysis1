# Science Assessment Question Extraction & Evaluation Prompt

## What I'm giving you:
PDF files of science assessments exported from our secure test browser. Each PDF contains multiple test questions (multiple choice, true/false, or open-ended).

## What I need you to do for EACH question in every PDF:

### 1. Extract the question content
- Question number
- Full question stem (exact text)
- Image/diagram description (detailed description of any visual — what it shows, what is labeled, what data is presented. "None" if no image.)
- All answer choices (A, B, C, D or True/False)
- Correct answer (if marked/identifiable)
- Grade level (if visible)
- Cited NGSS standard (if visible)
- Assessment/source name (from the PDF title or header)

### 2. Evaluate against the Achieve Cognitive Complexity Framework (2019)
Rate each of the 4 indicators on a 1-5 scale WITH full justification:
- **Scenario** (1-5) + justification — How puzzling/uncertain is the phenomenon?
- **SEP** (1-5) + justification — How are Science & Engineering Practices used for sense-making?
- **DCI** (1-5) + justification — How is science content used for sense-making?
- **CCC** (1-5) + justification — How do Crosscutting Concepts expand/focus thinking?

Assign a **Holistic Classification:**
- Scripted / Low Guided Integration / High Guided Integration / Doing Science

### 3. Evaluate against Achieve Assessment Criteria (2018)
Rate each criterion as Does Not Meet / Partially Meets / Meets:
- **Criterion 2** — Three-Dimensional Performance
- **Criterion 3** — Phenomena
- **Criterion 5** — Cognitive Complexity
- **Criterion 6** — Technical Quality

### 4. Assign an overall rating
- **Strong** / **Needs Improvement** / **Weak**

### 5. Provide a brief recommendation
- 1-2 sentences on the biggest issue or what would improve the question

## Output format: CSV-ready table with these columns:

| # | Column | Example |
|---|--------|---------|
| 1 | Assessment | "Grade 3 Life Science Unit 2" |
| 2 | Q# | 1 |
| 3 | Stem | "Which of the following is a fossil?..." |
| 4 | Image/Diagram Description | "Labeled cross-section of a vacuum flask showing inner glass layer, outer glass layer, vacuum gap, reflective coating, sealed lid, liquid inside. Arrows show heat transfer directions." or "None" |
| 5 | Type | MC / TF / Open |
| 6 | Choices | "A) Replica in museum B) Dinosaur bone still buried C) Full-size model D) Living lizard" |
| 7 | Correct Answer | B |
| 8 | Grade | 3 |
| 9 | NGSS Standard | 3-LS4-1 |
| 10 | Scenario (1-5) | 2 |
| 11 | Scenario Justification | "No phenomenon presented. No uncertainty to figure out. Students are asked to identify a definition, not figure out something puzzling." |
| 12 | SEP (1-5) | 1 |
| 13 | SEP Justification | "Standard requires 'analyze and interpret data.' Item requires identification/recall only — no data provided, no analysis required." |
| 14 | DCI (1-5) | 2 |
| 15 | DCI Justification | "Tests definitional knowledge of fossils. While grade-appropriate, it's direct recall, not reasoning with the DCI." |
| 16 | CCC (1-5) | 1 |
| 17 | CCC Justification | "No CCC engagement. No patterns, scale, or cause/effect reasoning required." |
| 18 | Indicator Avg | 1.5 |
| 19 | Holistic Classification | Scripted |
| 20 | Crit 2: Three-Dimensional | Does Not Meet |
| 21 | Crit 3: Phenomena | Does Not Meet |
| 22 | Crit 5: Complexity | Does Not Meet |
| 23 | Crit 6: Technical Quality | Partially Meets |
| 24 | Overall Rating | Weak |
| 25 | Key Recommendation | "No phenomenon present. Tests vocabulary recall only. Replace with data-interpretation item that provides fossil location data and asks students to draw conclusions about past environments." |

## Processing instructions:
- Process ALL questions in each PDF — don't skip any
- If a question is partially cut off or unreadable, flag it in the stem column as "[UNREADABLE]" and move on
- Keep evaluations consistent — use the same rubric standards across all questions and all PDFs
- For images/diagrams: describe what is shown in enough detail that someone who cannot see the image would understand what information the student is working with. Include labels, data values, axis titles, units, and any other visible details.
- After each PDF is processed, provide a summary count:
  - Total questions
  - Holistic breakdown: how many Scripted / Low Guided / High Guided / Doing Science
  - Overall breakdown: how many Strong / Needs Improvement / Weak
  - Average indicator scores across all questions
