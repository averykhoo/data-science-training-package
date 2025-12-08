code ~~fluency~~ craftsmanship competency

contrapositive definitions for pls so it's not taken as a checklist - maybe codify red flags?

clarify tech leadership as tech standards and strategy

add user empathy and elicitation to dpd pl2

explicitly say it's the complexity of the problem, not the solution 

L4 nlp without ml could be like a phd in computational linguistics 

is feature hashing in there?
also look into the mle books sent in telegram

---
---


Here is the comprehensive summary of the recommended changes to the Data Science Training Package and Competency Framework.

This synthesis integrates the **Theoretical Underpinnings** (Breiman, Dreyfus, Legal Theory), the **Motivating Factors** (current assessment failures), and the **Execution Details** required to modernize the framework.

---

### 1. The Competency Map (The Rubric)

This is the core of the framework. The shift is from assessing **Tools** (e.g., "Can you use XGBoost?") to assessing **Cognitive Intent** (e.g., "Why did you choose prediction over inference?").

#### **A. Reframing "Data Project Design" (The Strategic Wrapper)**
*   **The Problem:** Candidates currently view this as a "Soft Skill" (requirements gathering) and neglect scientific rigor. They treat it as the "warm-up" before the real work of coding begins.
*   **The Theory:** **The Scientific Method.** A project is not just code; it is a hypothesis validation loop. The "Design" is the architecture of that loop.
*   **The Fix: The "Bookend" Model.**
    *   **The Start (Translation):** Converting abstract business needs into precise technical proxies (e.g., "User Happiness" $\to$ "Retention Rate").
    *   **The Middle (Validation Strategy):** **(Crucial Shift)** Move "Experiment Design" from the Stats/ML bucket to here. DPD owns the *logic* of proof (e.g., "We need a time-based split because of seasonality"). Stats/ML owns the *implementation*.
    *   **The End (Synthesis):** Closing the loop. Did the technical proxy actually move the business metric?
    *   **Why:** This forces candidates to demonstrate **Strategic Integrity**—ensuring they aren't just building a perfect model for the wrong problem (Type III Error).

#### **B. Distinguishing "Stats vs. ML" (The Two Cultures)**
*   **The Problem:** Confusion over tools ("Is Logistic Regression Stats or ML?").
*   **The Theory:** **Leo Breiman’s "Two Cultures" (2001).**
    *   **Culture 1 (Stats):** Believes nature has an intelligible structure. Optimizes for **Inference**.
    *   **Culture 2 (ML):** Believes nature is complex/unknowable. Optimizes for **Prediction**.
*   **The Fix: Define by Intent and Validation.**
    *   **Statistical Analysis (Structure):**
        *   *Intent:* To understand *why* (Causality/Inference).
        *   *Validation:* **Ex Ante (Pre-flight).** checking assumptions (Normality, I.I.D.) *before* trusting the model.
        *   *Source of Truth:* The Expert/Theory.
    *   **Machine Learning (Scale):**
        *   *Intent:* To predict *what* (Generalization).
        *   *Validation:* **Ex Post (Crash Test).** Checking validation loss and generalization gaps *after* training.
        *   *Source of Truth:* The Data.
    *   **Bayesian Methods:** The "Tax" at both ends. Requires **Priors** (Structure) AND **Posterior Predictive Checks** (Simulation Fidelity).

#### **C. Redefining Proficiency Levels (Cognitive Complexity)**
*   **The Problem:** Candidates pass based on "Book Knowledge" (Polished L1) but fail when things go wrong in production.
*   **The Theory:** **The Dreyfus Model of Skill Acquisition** and **Kung Fu (Embodied Skill).**
*   **The Fix:**
    *   **PL2 (The Consultant): Add "Diagnostic Intuition" (Kung Fu).**
        *   *Definition:* The muscle memory to handle the unexpected. The ability to debug a system from first principles when the "Happy Path" breaks.
        *   *Why:* To filter out candidates who only know how to run a tutorial script.
    *   **PL3 (The Senior): Add "Parsimony" (Wisdom).**
        *   *Definition:* Knowing what *not* to build. The ability to reject complex, "shiny" solutions (like LLMs) in favor of simple, robust heuristics.
        *   *Why:* Seniority is defined by **Restraint** and **Architecture**, not just coding speed.

#### **D. Future-Proofing for AI (The Moving Baseline)**
*   **The Problem:** LLMs will automate L2 "Generation" tasks by 2026/27.
*   **The Theory:** **The Blockhead Argument.** AI has infinite knowledge (lookup table) but zero connection to physical reality.
*   **The Fix: Shift from Generation to Supervision.**
    *   **New L2:** **Verification.** The ability to audit AI output, spot hallucinations, and accept liability for the result.
    *   **New L3:** **Constraint Injection.** The ability to use Formal Specification to constrain the AI's search space to solutions that are robust and maintainable.

---

### 2. The Assessment Process (The Legal System)

The goal is to move from a "Filtering" system (rejecting unprepared candidates in the room) to a "Verification" system.

*   **The Problem:** High failure rates and "Polished Turds" (projects that look good because a mentor fixed them).
*   **The Theory:** **Conflict of Interest & Adversarial Justice.** A single person cannot effectively be the Defense Attorney (Coach) and the Judge (Assessor).
*   **The Fixes:**
    1.  **Strict Recusal:** An L3/L4 who acts as a **Sponsor** (Coach) *cannot* sit on the panel.
    2.  **Sponsors give Verdicts, not Solutions:** Pre-panel feedback should be "You are not ready because X," not "Change X to Y." This forces the candidate to do the synthesis work.
    3.  **Limit Testing (The PhD Defense):** The panel must probe until the candidate fails.
        *   *Pass:* Admitting ignorance at the boundary (Intellectual Honesty).
        *   *Fail:* BS-ing the expert (Integrity Violation).
    4.  **15/45 Time Split:** Cap presentations at 15 minutes. Use 45 minutes for probing "Negative Space" (what did you *not* do, and why?).

---

### 3. The Syllabus & Content (The Fuel)

The learning materials must align with the new rigour of the Competency Map.

*   **Modernization:**
    *   **ASR:** Archive Kaldi/GMMs. It is legacy tech.
    *   **NLP:** Shift focus from NLTK/Regex to **Transformers, Embeddings, and LLM APIs**.
*   **Projects:**
    *   **Retire Kaggle Titanic:** It suffers from massive data leakage and teaches nothing about Data Prep.
    *   **Introduce "Dirty Internal Mocks":** Provide messy, multi-table datasets that force candidates to practice **Data Project Design** (Formulation) and **Data Prep** (Cleaning/Joining) before they can even attempt the modeling.
*   **Cleanup:**
    *   Archive the old "Design/Build/Run" framework to prevent confusion with the new Functional Competencies.





---
---

Here is the enumeration of the items from your Todo list, contextualized with the details from the text block (which appears to be drawn from Wise and Amazon's SDE career maps).


note that this list was originally created 23 Nov 2023

### 1. The Todo List (Enumerated)

1.  **Split out any MLE stuff:** Ensure a clear distinction between Data Science competencies and Machine Learning Engineering competencies (e.g., deployment infrastructure vs. model development).
2.  **Mandatory Mentorship for Consultants:** An L2 (Consultant) requirement is added: they must have started mentoring or onboarding new officers.
    *   *Context:* This aligns with the "Lead Role" and "Coach and Mentor" definitions provided. The team must be "stronger because of your presence."
3.  **Data Hygiene Requirement:** "You gotta train on clean data." This reinforces the EDA/Data Prep competency.
4.  **Dataset Size Requirement:** Candidates must work on a sizeable dataset.
    *   *Context:* This targets the specific "Da (Data Analyst/Scientist) must work with large data" point. It acts as a filter against "toy problems."
5.  **The "Lowest Full Match" Principle:** "If you make PL1 mistakes, you are a PL1."
    *   *Context:* This is a critical assessment heuristic. High-level performance in one area does not cancel out fundamental incompetence in another. (e.g., A brilliant model trained on leaked data is still an L1 failure).
6.  **Principles of Design Thinking:** Explicitly incorporate design thinking into the DPD competency (empathy with users, iterative prototyping).
7.  **Whiteboarding:** Introduce a whiteboarding component (likely for system design or logic flow) to the assessment.
8.  **Engineering Career Map Benchmarking:** Review and align with the `wise.jobs` engineering career map.
    *   *Context:* Focus on "Dealing with Ambiguity," "Autonomy," and "Addressing Systemic Issues."
9.  **Red Flag Checks:** Explicit checks for disqualifying errors, such as "training on a broken golden set."
10. **Simplification:** Reduce the competency list to 5–10 core items to ensure the framework is memorable and usable.
11. **Code Craftsmanship:** Elevate code quality from "it works" to "it is maintainable."
    *   *Context:* Aligns with "Maintainability" (building foundations for the future) and "Demonstrating engineering best practices."
12. **Curriculum Resources:** Review the "MLE books on Telegram" for inclusion in the syllabus or reading lists.
13. **Clarify Data Project Design (DPD):** Address the ambiguity regarding experiment design and conduct.
    *   *Note:* We addressed this in the previous turn by moving "Validation Strategy" into DPD.
14. **Language Policy:** Python is mandatory; R is a permitted addition but not a substitute.

---

### 2. Solving the "Scalable Code Review"

You raised a critical constraint: **How do you review code integrity without burning out your 3 panelists or relying on a conflicted Sponsor?**

If you cannot afford a full asynchronous code audit by a neutral party, you must integrate the review into the **Panel Process itself** or use **Automated Gates**.

Here are three scalable strategies, ranked from "Low Effort" to "High Impact."

#### Strategy A: The Automated Gate (The "Hygiene" Check)
*   **The Mechanism:** Require candidates to submit their repo link 48 hours before the panel. Run a standard linter/static analyzer (e.g., `flake8`, `pylint`, or a cyclomatic complexity checker) and a notebook scanner (e.g., checking for out-of-order execution).
*   **The Rule:** If the code scores below a threshold (e.g., Score < 7/10), the panel is **automatically cancelled**.
*   **Why it works:** It forces the candidate to police themselves. You don't waste human time reviewing code that is syntactically messy.
*   **Scalability:** Infinite. It’s a script.

#### Strategy B: The "Code Walk" (The "Spot Check")
*   **The Mechanism:** Dedicate 5–10 minutes of the Q&A specifically to a live code inspection.
*   **The Tactic:** Do not let them choose what to show. The "Engineering" Panelist (Zone C) chooses a file at random from their repo during the call.
    *   *"Please open `preprocessing.py`. Walk me through lines 40 to 60. Why did you implement the null imputation this way?"*
*   **The Signal:**
    *   **L1:** Struggles to explain their own code (implies copy-paste or lack of understanding).
    *   **L2:** Explains the logic clearly.
    *   **L3:** "Oh, that part is actually ugly because I had to work around a legacy data format..." (Honesty/Context).
*   **Scalability:** High. Zero prep time required for panelists.

#### Strategy C: The "Readability" Heuristic (The 5-Minute Scan)
*   **The Mechanism:** The "Engineering" Panelist spends exactly 5 minutes scanning the repo *before* the panel (during the pre-huddle). They aren't looking for bugs; they are looking for **Empathy**.
*   **The Question:** "If I fell into a coma and woke up tomorrow, could I run this code based solely on the README and the variable names?"
*   **The Heuristic:**
    *   No `requirements.txt`? $\to$ **Fail.**
    *   Hardcoded paths (`/Users/steve/desktop/data.csv`)? $\to$ **Fail.**
    *   Functions named `func1`, `do_stuff`? $\to$ **Fail.**
*   **Why it works:** You aren't judging the *algorithm* (you do that in Q&A). You are judging the **Professionalism** (Code Craftsmanship).

### Recommendation
Adopt **Strategy B (The Code Walk)** immediately.
It fits perfectly into your "15+45" time split (put it in the Engineering Zone time block). It terrifies candidates into actually learning their codebase, and it exposes "Polished Turds" instantly because they can't defend code they didn't really write.


---
---

You are looking for a way to define **Necessary Conditions** rather than **Sufficient Conditions**.

A checklist implies sufficiency: *"If I tick all these boxes, I am L2."*
A waterline implies necessity (the contrapositive): *"If I **cannot** comfortably do these things, I am **not** L2."*

Here is how to phrase this "Contrapositive Assessment" to kill the checklist mentality, along with a concrete way to add it to your documentation.

### 1. The Core Philosophy: "The Struggle Test"

The difference between a "Checklist Item" and a "Behavioral Indicator" is **Ease**.
*   **Checklist:** "I did it once (maybe with a lot of help)."
*   **Indicator:** "I can do it on a bad day, with a headache, without asking for help."

**The Contrapositive Definition:**
> *"The descriptors below represent the **baseline reliability** expected at this level. You are not at this level because you have **performed** these tasks; you are at this level because you **no longer struggle** with them."*

### 2. The Contrapositive Phrasing for each Level

You can add these "Litmus Tests" to the top of each level definition (`dsai-l2.md`, etc.) to frame the mindset before they read the bullets.

#### **For L1 (The Novice)**
*   **The Positive:** "Executes routine tasks."
*   **The Contrapositive (Litmus Test):**
    > "If you are blocked by standard syntax errors, library installation issues, or basic data cleaning steps, and require a senior to unblock you on these 'mechanics', you are not yet fully L1."

#### **For L2 (The Consultant / Kung Fu)**
*   **The Positive:** "Solves standard problems independently."
*   **The Contrapositive (Litmus Test):**
    > "If you encounter a messy dataset, a vague requirement, or a model error and your first instinct is to **stop and ask 'What should I do?'** rather than proposing a solution, you are not L2."
    >
    > *"L2 is the absence of dependency on L3 for standard execution."*

#### **For L3 (The Senior / Wisdom)**
*   **The Positive:** "Navigates ambiguity and complex systems."
*   **The Contrapositive (Litmus Test):**
    > "If you solve a technical problem but create a downstream organizational headache (e.g., technical debt, stakeholder confusion, maintenance nightmare) because you didn't look at the bigger picture, you are not L3."
    >
    > *"L3 is the absence of tunnel vision."*

### 3. How to write this in the Intro Doc

You should update `dsai-intro.md` to explicitly kill the checklist. Here is a blurb you can copy/paste:

---

### **How to Read the Competency Maps**

**These are NOT Checklists.**
Completing a task listed in PL2 once does not make you PL2.
These descriptors are **Waterline Indicators**. They represent the level of work that should feel **routine** to you.

**The "Reliability" Rule:**
Assessment is based on **Reliability**, not **Peak Performance**.
*   **PL1:** You can reliably execute the task if given a guide.
*   **PL2:** You can reliably execute the task if given a problem.
*   **PL3:** You can reliably define the task if given a goal.

**The Contrapositive Test:**
When assessing yourself, ask: *"If I were given this task today, under time pressure, would I need guidance to finish it?"*
*   If the answer is **Yes**, you have not yet mastered this Proficiency Level, even if you have "done it before."

---

### 4. Why this helps the Panel

This phrasing arms your panelists (especially the PhDs) with a powerful argument against the "Polished" candidate.

*   **Candidate:** "But I showed you the slide where I calculated the VIF! That's on the L2 checklist!"
*   **Panelist:** "Yes, you did it. But when I asked *what* VIF measures, you struggled. This indicates you cannot do it **reliably** without a guide. Therefore, you fail the Contrapositive test."

It shifts the conversation from **"Did you do it?"** to **"Do you own it?"**
