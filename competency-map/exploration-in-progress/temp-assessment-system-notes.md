You are absolutely correct that this requires more than just having a curriculum. You prove your system has learning
outcomes by creating a robust **Assessment System**. This system is the engine that measures a learner's performance
against the standards you've set.

Let's break down exactly what this means and how to build it.

### Step 1: Recognize Your Learning Outcomes Already Exist

First, a crucial clarification. You don't need to *add* learning outcomes. **The Proficiency Level (PL) descriptors in
your Competency Map *are* your learning outcomes.**

A learning outcome is a clear, measurable statement of what a student should be able to *do*.

* The learning outcome for a **PL2 in Machine Learning** is not "to know about machine learning." It is: "The learner
  will be able to ensure the test set has no leakage, ensemble, regularize, tune, and evaluate models."
* The learning outcome for a **PL3 in Data Project Design** is: "The learner will be able to break down complex / vague
  business goals into well-defined requirements and constraints."

Your entire system is already built on a foundation of well-defined, behavioral learning outcomes. Your challenge isn't
creating them; it's **proving** they have been achieved.

### Step 2: Build an Assessment System to "Prove" the Outcomes

This is the system that answers the question, "Exams? Projects?" The answer is that both are types of **assessment
instruments**, but for your purposes, one is far superior.

A complete assessment system has four components:

#### A. The Assessment Instruments (The "Evidence")

These are the tools you use to collect evidence of a learner's abilities. You have two main choices:

1. **Traditional Assessment (Exams):**
    * **What it is:** Multiple-choice questions, short-answer tests, and standardized exams.
    * **Pros:** Scalable, easy to grade, good for testing factual recall and procedural knowledge (PL1).
    * **Cons:** Very poor at testing higher-order skills like analysis, synthesis, and creation (PL2+). They don't
      reflect how real work is done.
    * **Verdict for you:** Largely inappropriate. You don't care if someone can define "boosting"; you care if they can
      *use* it to solve a problem.

2. **Authentic Assessment (Projects):**
    * **What it is:** A task that requires learners to perform in a way that realistically mimics the work of a
      professional in the field.
    * **Pros:** Directly measures the skills you care about. Requires synthesis of knowledge across multiple
      competencies. Produces a tangible artifact (code, analysis) and demonstrates real-world problem-solving.
    * **Cons:** Less standardized and more time-consuming to evaluate.
    * **Verdict for you:** **This is your gold standard.** Your existing plan to use Kaggle projects and real OJT
      assignments is the *correct* pedagogical choice.

Your system's "evidence" should therefore be two things:

1. **The Project Artifact:** The final Jupyter Notebook, the Git repository with clean code, the API they built.
2. **The Project Defense:** The presentation where they explain and defend their work.

#### B. The Rubric (The "Standard of Proof")

This is the standard against which you measure the evidence.

* **Your `competency-map` IS this rubric.** This is its most important function.
* During an assessment, every piece of evidence the candidate presents is mapped back to the rubric.
    * *When the candidate explains their choice of evaluation metric...* the assessor is checking for evidence of the *
      *PL2 ML** behavior: "Evaluate, describe, and make detailed comparisons of model performance..."
    * *When the candidate presents a confusing chart...* the assessor notes a gap against the **PL2 Storytelling**
      behavior: "Design clean and comprehensible visualizations."
    * *When the candidate describes how they translated the business need into a data problem...* the assessor is
      looking for evidence of the **PL2 Project Design** competency.

#### C. The Assessors (The "Judges")

These are the people who use the rubric to evaluate the evidence.

* **Who they are:** A panel consisting of you and other senior team members or mentors.
* **The Critical Requirement: Calibration.** The biggest risk in any assessment system is subjectivity. "Calibration" is
  the process of ensuring all assessors interpret the rubric in the same way. Before a round of assessments, the panel
  should meet to discuss one or two examples to make sure they are aligned. Your `dsai-tech-panel-form-l2.md` is a tool
  that helps enforce this consistency.

#### D. The Process (The "Trial")

This is the formal event where the assessment takes place.

* **What it is:** The panel presentation and Q&A session.
* **How it works:** The candidate presents their project (the evidence). The panel listens and asks probing questions.
  The questions are a key part of the assessment, designed to differentiate between proficiency levels. You have already
  designed these! The file `competency-map/bonus-content-proficiency-level-definitions.md` provides the exact questions
  to use:
    * To test PL1 vs. PL2: "Why was this statistical test the right one? What other standard methods did you consider?"
    * To test PL2 vs. PL3: "What were the most significant assumptions you made? What was your plan B?"

### The System in Action: A Worked Example

1. **Goal:** An L1 Data Scientist wants to be promoted to L2 (Consultant).
2. **Learning Outcomes:** They consult the `competency-map` and see they need to demonstrate PL2-level behaviors across
   most competencies.
3. **The Curriculum:** They undertake a real **OJT project** that is complex enough to allow them to demonstrate these
   behaviors. They use the curated curriculum (videos, articles) to fill their knowledge gaps.
4. **The Assessment:**
    * **Instruments:** They produce a final project notebook and a presentation summarizing their work and its impact.
    * **Process:** They present to a calibrated **panel of assessors**.
    * **Rubric:** The panel uses the **Competency Map** as their rubric to evaluate the presentation and the project
      artifacts. They use the targeted questions from the bonus content to probe the candidate's depth of understanding.
5. **The Proof:** The outcome is a filled-out evaluation form (`dsai-tech-panel-form-l2.md`) with specific,
   evidence-based justifications for why the candidate has (or has not) met the learning outcomes for the L2 level.

This creates a complete, defensible system that **proves** learning outcomes have been met by measuring authentic work
against a clear and explicit standard.