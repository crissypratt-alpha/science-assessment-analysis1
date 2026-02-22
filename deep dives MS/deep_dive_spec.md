# Deep Dive Output Specification (v1.0)

This document defines the **exact, required structure** for all student deep dives.
All deep dives must follow this specification **exactly**.

Deviation is not allowed.

---

## GENERAL RULES

- One deep dive per student.
- Output format: **Markdown (.md)** only.
- File naming convention:

- Section titles, order, table headers, and column order must match this spec exactly.
- Do **not** add extra sections.
- Do **not** rename columns.
- If data is missing or unavailable, write **`MISSING`** in the cell and explain in Section 6 (Evidence).
- All calculations must be reproducible from the values shown.

---

## SECTION 1 — Student Snapshot

**Purpose:** Establish identity, placement, and instructional context.

### Table 1.1 — Student Snapshot

| Student | Campus | Enrollment Grade | Current Course | Age Grade | Course Grade | Highest Mastered Grade (HMG) |
|--------|--------|------------------|---------------|-----------|--------------|------------------------------|

**Definitions**
- **Enrollment Grade**: grade level assigned by enrollment.
- **Age Grade**: chronological grade level.
- **Course Grade**: nominal grade level of the current course.
- **HMG**: highest fully mastered grade level (not “working in”).

---

## SECTION 2 — Course Progress & Effort

**Purpose:** Quantify progress and time investment.

### Table 2.1 — Course Progress

| % Complete | Total XP Earned | Total XP Remaining | Time in Course (days) | Avg XP / School Day |
|------------|----------------|--------------------|------------------------|---------------------|

**Rules**
- **Time in Course (days)** = number of unique school days with recorded activity.
- **Avg XP / School Day** = Total XP Earned ÷ Time in Course (rounded to 1 decimal).
- XP Remaining must be shown even if % Complete is low.

---

## SECTION 3 — Assessment & Practice Signals

**Purpose:** Distinguish mastery checks from practice behavior.

### Table 3.1 — Assessment & Practice

| Test Attempts | Last Test Date | Hole-Filling Attempts | Accuracy Trend | Fluency Signal |
|--------------|---------------|------------------------|----------------|----------------|

**Allowed Values**
- **Accuracy Trend**: Improving / Flat / Declining / Insufficient data
- **Fluency Signal**: At level / Below level / Not assessed

---

## SECTION 4 — Learning Velocity & Growth

**Purpose:** Determine whether learning rate meets expectations.

### Table 4.1 — Growth Metrics

| Growth X | Expected Growth X | Meets 2× Target? | Notes |
|--------|-------------------|------------------|-------|

**Rules**
- **Expected Growth X** defaults to **2.0** unless explicitly specified otherwise.
- **Meets 2× Target?** = Yes / No
- **Notes** must reference concrete data from prior sections.

---

## SECTION 5 — MAP Growth Context

**Purpose:** Surface alignment or mismatch between instruction and MAP sampling.

### Table 5.1 — MAP Profile

| MAP Math RIT | MAP Grade Band | Domains Missed | Alignment Risk |
|-------------|----------------|----------------|----------------|

**Rules**
- **Domains Missed** must list actual MAP domain names.
- **Alignment Risk** = Low / Medium / High
- **High Risk** indicates insufficient exposure to grade-band domains MAP assesses.

---

## SECTION 6 — Root Cause Analysis

**Purpose:** Identify the primary reason the student is not further along.

### Primary Root Cause (choose exactly ONE)

- Placement mismatch
- Insufficient time on task
- Accuracy constraint
- Fluency constraint
- MAP–curriculum misalignment
- Coasting / low intensity
- Data quality issue

### Secondary Root Cause (optional, choose at most ONE)

### Evidence (required)

- Bullet list
- Each bullet must explicitly cite a metric or table from Sections 2–5
- No opinions without data support

---

## SECTION 7 — Completion Projection

**Purpose:** Quantify feasibility of finishing by end of year.

### Fixed Assumptions
- XP per day = **25**
- Days per week = **5**

### Table 7.1 — Projection

| XP Remaining | XP / Day Assumed | Days / Week | Weeks to Finish | Finish Before EOY? |
|--------------|------------------|-------------|------------------|--------------------|

**Rules**
- Weeks to Finish = XP Remaining ÷ (25 × 5), rounded **up**.
- **Finish Before EOY?** = Yes / No / Borderline

---

## SECTION 8 — Intervention Levers

**Purpose:** Identify immediate, actionable changes.

### Actions (maximum 5 bullets)

- Each action must map directly to the identified root cause.
- Actions must be operational and time-bound.
- Avoid philosophical or vague language.

---

## REQUIRED VALIDATION CHECKLIST (must appear at bottom)

- [ ] All required sections are present
- [ ] All tables match the specified column headers and order
- [ ] Exactly one primary root cause selected
- [ ] All computed values can be traced to displayed data
- [ ] Projection math uses fixed assumptions (25 XP/day, 5 days/week)

---
