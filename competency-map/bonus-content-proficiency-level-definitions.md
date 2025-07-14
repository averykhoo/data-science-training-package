(written with help from gemini)

| PL  | Level Name               | Core Concept (Bloom's)                         | Cognitive Skill (Bloom's)                                                                | Problem & Task Scope                                                                                                                         | Dominant Knowledge Type                                                                                                                 | Learner & Practitioner Model (Dreyfus)                                                               | Culinary Analogy                                                                                                                  |
|:----|:-------------------------|:-----------------------------------------------|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| PL1 | Foundational Application | **Execute** a common procedure                 | **Remembering** and **applying** processes and rules and following steps                 | **Routine Tasks:** Well-defined, with clear instructions, and a known correct output                                                         | **Factual & Procedural:** Knowing terminology, syntax, and the specific steps of a "recipe"                                             | Novice: Rigidly follows rules without a full grasp of context                                        | Can flawlessly follow an existing recipe to the letter. They know *what* to do and in what order, but may not know *why* it works |
| PL2 | Independent Application  | **Solve** a standard problem independently     | **Understanding** principles and **evaluating** options to select the appropriate method | **Standard Problems:** Non-trivial, requiring independent diagnosis, and use of standard methodologies                                       | **Conceptual:** Understanding the "why" behind the methods, their principles, theories, and standard use cases                          | Competent: Can troubleshoot and solve problems independently; develops a working model of the domain | Understands the principles behind recipes. Can select the best recipe for an occasion and make intelligent substitutions          |
| PL3 | Adaptive Synthesis       | Diagnose and navigate complexity and ambiguity | **Analyzing** assumptions **evaluating** trade-offs to **synthesize** custom solutions   | **Complex & Ambiguous Problems:** Open-ended, complex, or ambiguous; lacking a single, pre-defined "right answer"                            | **Procedural:** Mastery of evaluation criteria, awareness of methodology limitations, and ability to adapt/combine techniques           | Proficient: Sees situations holistically and intuitively prioritizes what's important                | Can invent a new dish on the fly by adapting and combining techniques to suit a "mystery box" of unexpected ingredients           |
| PL4 | Generative Creation      | **Invent** new, generalizable capabilities     | **Creating** novel solutions by reflecting on the problem space itself                   | **Generative Problems:** Unforeseen challenges or strategic opportunities; creating a generalizable system or framework that empowers others | **Metacognitive:** Self-awareness of methods, understanding the limits of current knowledge, and defining new ways to approach problems | Expert: Performance is fluid and intuitive; no longer relies on explicit rules                       | Doesn't just invent one new dish, but creates a new system or technique (like *sous-vide* or books like *Modernist Cuisine*)      |

---

(taking an analogy half a step too far)

| PL  | **The Recipe Analogy**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:----|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PL1 | **The Line Cook:** Can flawlessly follow an existing recipe to the letter. They know *what* to do and in what order. If you ask for the recipe's Coq au Vin, you will get that exact Coq au Vin. They might not know *why* searing the chicken before braising is crucial, but they know the recipe says to do it, and they do it perfectly every time.                                                                                                                                                                                                         |
| PL2 | **The Confident Home Chef:** Understands the principles *behind* the recipes. They have a repertoire of dishes they know well. They can look at five different roast chicken recipes and select the best one for the occasion. Critically, they can make intelligent substitutions - using shallots instead of onions, or olive oil instead of butter - because they understand the *function* of the ingredients. They can tweak a recipe to make it slightly better.                                                                                          |
| PL3 | **The Restaurant Chef / "Iron Chef":** Can invent a new dish on the fly to solve a complex, ambiguous problem. You give them a "mystery box" of unexpected ingredients (a messy dataset, unusual constraints) and a goal ("make a savory entree"). They will analyze the ingredients' properties, evaluate multiple techniques, and synthesize a novel, coherent, and delicious dish by adapting and combining principles from dozens of recipes they have mastered. Their creation is custom-built for that specific, unique situation.                        |
| PL4 | **The Culinary Innovator (e.g., a McGee or Achatz):** Their focus is not on creating just one new dish, but on creating a new *system, framework, or technique* that empowers thousands of other chefs. They don't just invent a dish; they invent *sous-vide* cooking. They don't just write a recipe; they write **"Larousse"** - a book that codifies the fundamental principles of good cooking, giving others a framework to create their *own* dishes. Their output is a high-leverage tool or a mental model that enables and elevates the entire field. |

---

### How to Use This Table

This table serves as the "constitution" for the competency framework. It provides a shared, calibrated language for
individual contributors, managers, and technical assessors to discuss and evaluate skill progression.

1. **For Individual Contributors:** It provides a detailed roadmap for career growth. To move from PL1 to PL2, a data
   scientist can see they need to shift their focus from mastering *steps* (**Procedural Knowledge**) to mastering
   *principles* (**Conceptual Knowledge**). It clarifies that advancement comes from a deeper and more abstract level of
   understanding, not just completing more tasks.

2. **For Managers & Mentors:** It gives them a precise, multi-faceted language for feedback. Instead of saying "you need
   to be more independent," a manager can say, "You are operating at a strong PL1 by flawlessly executing the playbooks
   we give you. To reach PL2, I want you to start focusing on the *conceptual* aspect: for your next project, propose
   which of our standard approaches is most suitable and explain why, rather than waiting for the method to be
   assigned."

3. **For Assessors & Panelists:** It is the ultimate calibration tool. It trains them to look beyond the surface-level
   complexity of a presented project and to probe for the *thinking* behind it. It provides a foundation for asking
   questions that differentiate skill levels.

---

### Differentiating the Proficiency Levels in Practice

Use these targeted questions during technical discussions or panel assessments to accurately pinpoint an individual's
proficiency level:

* **To test for PL1 (Foundational Application):**
    * "Can you walk me through the exact steps you took to get this result?"
    * *Focus:* The emphasis is on the correct and reliable execution of a known, pre-defined procedure.

* **To differentiate PL1 from PL2 (Independent Application):**
    * "Why was this statistical test the right one to use here? What other standard methods did you consider, and why
      were they less appropriate?"
    * *Focus:* This probes for the shift from *how* (procedure) to *why* (concept). A PL2 can justify their choice from
      a set of known alternatives based on underlying principles.

* **To differentiate PL2 from PL3 (Adaptive Synthesis):**
    * "What were the most significant assumptions you made? What would have happened if those were violated, and what
      was your plan B? Can you walk me through the trade-offs of the different approaches you evaluated before designing
      this custom solution?"
    * *Focus:* This probes for the ability to navigate ambiguity. A PL3 can analyze, evaluate, and synthesize a novel
      solution when no standard playbook applies.

* **To differentiate PL3 from PL4 (Generative Creation):**
    * "The custom solution you built for this project is excellent. How would you generalize it? What would a framework,
      library, or methodology guide look like so that ten other teams could solve *similar* problems without your direct
      help?"
    * *Focus:* This probes for the shift from solving one complex problem to creating a high-leverage, reusable
      capability that empowers others. A PL4's output is often a tool or system for others to use.

---

### Explanations of Dominant Knowledge Types

* **Factual & Procedural (PL1):** This is the "what" and "how-to." It is the knowledge of terminology (e.g., "what is a
  confusion matrix?") and the knowledge of steps in a recipe (e.g., "how do I run a model in scikit-learn?"). It enables
  correct execution without a deep understanding of the underlying theory.

* **Conceptual (PL2):** This is the "why." It's the knowledge of principles, theories, and models. Instead of just
  following the recipe, a person with conceptual knowledge understands *why* a certain model is appropriate for a given
  data type and business problem.

* **Procedural (PL3):** At this level, "Procedural" refers to an advanced mastery *about* procedures. It's not just
  knowing individual recipes, but knowing how to compare, evaluate, adapt, and combine them. It's the knowledge of
  evaluation criteria and methodology limitations that allows one to synthesize a custom workflow when standard ones
  fail.

* **Metacognitive (PL4):** This is "thinking about thinking" or "knowledge about one's own knowledge." A person at this
  level reflects on the entire problem-solving process to invent better ways to create. They might conclude, "Our
  standard way of thinking about this problem is flawed; I need to create a new mental model and a framework to support
  it."

---

It's possible to create special cases, but a far more elegant and powerful solution is to **create a single, unified PL
definition that works for both functional and ancillary competencies.**

The reason this is possible is that the proficiency levels are not about the *subject matter* (like "Machine Learning"
or "Leadership"); they are about the **cognitive process and scope of impact** an individual demonstrates within that
subject. They measure the *how* and the *why*, not just the *what*.

Here is a proposed unified definition for the Proficiency Levels, designed to be universal across all your competencies.

---

### A Unified Proficiency Level "Constitution"

| PL      | Level Name                   | Core Cognitive Skill                        | Scope of Work                                                                                                                                | Primary Impact                                                                                                               |
|:--------|:-----------------------------|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| **PL1** | **Foundational Application** | **Execute a known procedure.**              | **Routine Tasks:** Following a clear, pre-defined process or "recipe."                                                                       | **Correctness:** The task is completed reliably and according to spec.                                                       |
| **PL2** | **Independent Application**  | **Solve a standard problem independently.** | **Well-Defined Problems:** Selecting the appropriate standard method or principle to achieve a goal.                                         | **Value & Reliability:** A complete, valuable piece of work is delivered without needing close supervision.                  |
| **PL3** | **Adaptive Synthesis**       | **Navigate ambiguity and complexity.**      | **Complex & Ambiguous Problems:** Analyzing trade-offs and synthesizing a custom solution when no standard "recipe" applies.                 | **Effective, Custom Solutions:** A novel solution is architected that effectively solves a unique and challenging problem.   |
| **PL4** | **Generative Creation**      | **Invent a new, generalizable capability.** | **Strategic & Generative Problems:** Reflecting on the problem space itself to create a new tool, framework, or system that empowers others. | **Leverage & Empowerment:** The output is not just one solution, but a "force multiplier" that enables many other solutions. |

---

### How This Unified Definition Applies to Both Competency Types

This universal definition works because it focuses on abstract skills that manifest differently in each competency.
Let's see how it applies to a functional competency (`Machine Learning`) and your two ancillary competencies (
`Technical Leadership`, `Community Contribution`).

| PL      | Machine Learning (Functional)                                                                                                                                                                                      | Technical Leadership (Ancillary)                                                                                                                                                                                       | Community Contribution (Ancillary)                                                                                                                                                                       |
|:--------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PL1** | **Executes a known procedure:** Can correctly train a standard XGBoost model using a pre-defined script and data pipeline.                                                                                         | **Executes a known procedure:** Reliably follows the team's established coding standards and version control process for their own work.                                                                               | **Executes a known procedure:** Successfully integrates into the team by following the documented onboarding process and learning from provided materials.                                               |
| **PL2** | **Solves a standard problem:** For a standard classification task, can independently select between Logistic Regression, XGBoost, or a Random Forest, justifying their choice based on the data and project goals. | **Solves a standard problem:** Independently guides a junior team member through a well-defined technical task, explaining the standard approach clearly.                                                              | **Solves a standard problem:** Independently prepares and delivers a clear and valuable sharing session on a standard topic to the team.                                                                 |
| **PL3** | **Navigates ambiguity:** Faced with a novel problem (e.g., unusual data, complex constraints), they analyze the limitations of standard models and synthesize a custom architecture or loss function to solve it.  | **Navigates ambiguity:** When no best practice exists, they analyze the trade-offs of multiple potential solutions and architect a new, robust system design for the team to follow.                                   | **Navigates ambiguity:** Mentors a team member through an open-ended project, helping them analyze options and synthesize their own solution. Takes initiative to fill a knowledge gap in the community. |
| **PL4** | **Invents a new capability:** Designs and builds a new, reusable modeling library or framework that enables ten other data scientists to solve a whole class of problems more efficiently.                         | **Invents a new capability:** Conceives of and establishes a new set of technical standards or best practices (e.g., for MLOps or API design) that is adopted across the organization, creating leverage for everyone. | **Invents a new capability:** Designs and leads a new, scalable community program (like this entire DSAI framework) that systematically raises the skill level of the whole department.                  |

As you can see, the **core cognitive skill** and **scope of impact** are identical at each PL, whether you are writing
code, leading a design discussion, or mentoring a colleague.

**Conclusion:**

You absolutely can, and should, use a unified PL definition. It is the more robust and elegant design choice. It creates
a single, fair, and consistent "ruler" to measure all forms of professional growth, reinforcing the idea that
advancement comes from a deeper level of thinking and a broader scope of impact, regardless of the specific competency
being demonstrated. This makes the entire framework simpler to understand, communicate, and apply.