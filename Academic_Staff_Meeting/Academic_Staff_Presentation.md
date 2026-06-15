# Developing a Reproducible, Interactive Statistics Course

Audience: academic staff  
Length: 10-20 minutes  
Course: Statistics for third-year BSc Physics students, University of Groningen  
Core message: the course is not only about statistics content; it is also a reproducible, editable, computational learning environment.

---

## 1. Opening: what I built

I developed a new statistics course for third-year BSc Physics students.

- 12 interactive lecture notebooks
- Google Colab links for in-class execution
- GitHub repository students can fork and edit
- Two student workflows: quick access through Colab, or a local VS Code/Git setup for more durable work
- Board-style lecture notes in LaTeX
- Tutorial quizzes, assignments, project material, and exams/rubrics
- Development workflow running from the HPC, synchronized with Git and Overleaf

Speaker notes:

Start with the problem: statistics is easiest to learn when students can see equations, simulations, data, and inference procedures in the same place. The course was designed so students do not just read about statistics; they run it, change it, and inspect what happens.

Time: 1-2 minutes

---

## 2. The teaching problem

Traditional statistics teaching often separates three things that students experience as one problem:

- mathematical notation
- computational implementation
- interpretation of real data

In physics, this separation is especially artificial. Students need to move between probability models, code, plots, uncertainty, and scientific judgment.

Speaker notes:

Frame this as a pedagogical motivation rather than a technology pitch. The technology matters because it lets the teaching mirror the actual practice of data analysis in physics.

Time: 1-2 minutes

---

## 3. Design principle: one executable document

Each lecture is a Jupyter notebook.

- Text, equations, Python code, figures, and exercises live together.
- Students can open the material directly in Google Colab.
- Students who want more control can fork the repository and work locally, for example in VS Code.
- During class, they can run the same code I am discussing.
- After class, they can fork the full course and modify it freely.

Speaker notes:

Emphasize that the notebook is both a lecture note and a lab bench. A static derivation becomes an object students can interrogate: change a prior, increase the noise, add outliers, rerun a sampler, compare results.

Time: 2 minutes

---

## 4. Course arc

The lectures move from foundations to modern inference:

- Lectures 1-4: introduction, probability, distributions, correlations
- Lectures 5-7: classical/frequentist inference, likelihoods, model comparison, bootstrap
- Lectures 8-12: Bayesian inference, marginalization, MCMC, PyMC, Gibbs sampling, nested sampling, dynesty, PolyChord

Speaker notes:

This slide shows that the computational format is not a gimmick; it supports a serious conceptual arc. The later topics benefit strongly from executable examples, because students can watch sampling and model comparison happen rather than seeing only final formulas.

Time: 1-2 minutes

---

## 5. What students actually receive

The student-facing repository contains:

- lecture notebooks with Colab access
- datasets and figures used in class
- assignment notebooks
- tutorial quiz material where appropriate
- templates for written/project work

Private or controlled material is handled separately:

- exams
- rubrics
- solution material
- private Overleaf/Git repositories where needed

Speaker notes:

Make the access model clear. Students benefit from openness where it helps learning, while exam integrity and solution control are preserved.

Time: 1 minute

---

## 6. Live workflow for students

Students have two routes.

Route 1: Colab, the low-barrier option.

1. Open the notebook through the Colab badge.
2. Read the explanation and equations.
3. Run the code cells while the concept is introduced.
4. Modify parameters or code during exercises.
5. Save a personal copy when they want to keep their changes.

Route 2: VS Code and Git, the more flexible option.

1. Fork or clone the repository.
2. Open the course locally in VS Code.
3. Edit notebooks and files directly.
4. Commit changes and maintain their own version.

Speaker notes:

This is a good moment for a 60-second demo: open the GitHub repository, click "Open in Colab", run one small cell, then change a parameter. Then briefly mention the second route: Colab is excellent for access and in-class work, but local work through VS Code and Git is better when students want persistent edits, full control over files, and a proper personal fork. Colab sessions are convenient, but students need to save their work explicitly because temporary runtime state does not persist in the same way as a local repository.

Time: 1-3 minutes

---

## 7. Development workflow

My development environment is centered on the HPC.

- I can access the same course workspace from all my machines.
- The course repository is cloned and version controlled there.
- LaTeX material from Overleaf is Git linked and cloned on the HPC.
- Notebook, LaTeX, assignment, and exam development happen in one consistent environment.

Speaker notes:

The HPC is not just for computation here. It is a stable, always-available academic workspace. This makes course development less fragmented across laptops, browser tabs, and local folders.

Time: 1-2 minutes

---

## 8. How AI helped

I used AI as a course-development assistant, not as an autopilot.

Examples:

- improving explanations inside notebooks
- converting notebook content into board-style lecture notes
- drafting tutorial questions and assignments from lecture material
- generating and revising project ideas
- drafting mock and real exam questions with rubrics
- checking consistency between learning goals, notebooks, assignments, and assessment
- helping edit LaTeX directly in Git-linked Overleaf projects
- maintaining repositories: checking changes, preparing commits, pushing updates, and keeping student-facing and private material separated

Speaker notes:

Be explicit about the human role: AI speeds up drafting, variation, editing, consistency checks, and repository maintenance, but I remain responsible for correctness, level, assessment design, final wording, and what is pushed.

Time: 2 minutes

---

## 9. The AI workflow in practice

The practical loop is:

1. Course material lives in Git repositories on the HPC.
2. I ask Codex or Claude to work directly on notebooks, TeX files, or rubrics.
3. I inspect diffs and outputs.
4. I run notebooks or compile LaTeX when needed.
5. I commit and sync student-facing or private material to the right remote.

Speaker notes:

This is the key "how I developed it" slide. Stress version control and review. AI is useful precisely because the material is structured: notebooks, TeX, Git history, and a clear folder layout give the assistant context and make its changes inspectable. I also explain basic Git workflows to students, but for long-term course maintenance AI is very effective at the repetitive parts: identifying changed files, preparing sensible commits, pushing to the right repository, and keeping public and private material apart.

Time: 2 minutes

---

## 10. Benefits for teaching

This setup changes what is possible in the course.

- Students can reproduce every computational example.
- Exercises can be closer to real research practice.
- Lectures, assignments, and exams can be kept aligned.
- Updates are easier because material is version controlled.
- Colleagues can inspect, reuse, or adapt parts of the course.
- Students see transparent scientific workflows: code, data, assumptions, uncertainty.

Speaker notes:

Connect benefits to academic values: reproducibility, transparency, student agency, and maintainable teaching materials.

Time: 1-2 minutes

---

## 11. Challenges and safeguards

There are also important constraints.

- Colab lowers the technical barrier, but students still need guidance.
- Colab sessions are convenient but temporary; students need to save copies or use Git if they want persistent work.
- A local VS Code/Git setup gives more flexibility, but requires more initial setup.
- Notebooks can hide complexity if they are not structured carefully.
- AI-generated material must be checked for correctness and level.
- Private assessment material needs separate repositories and access control.
- Version control helps, but it requires discipline.

Speaker notes:

This slide makes the presentation credible. The message is not "AI solves course development"; the message is that a structured workflow makes AI useful while keeping academic control.

Time: 1-2 minutes

---

## 12. What I would like colleagues to take away

The main innovation is the integration:

- executable lectures
- student-owned copies through GitHub/Colab or local VS Code/Git workflows
- LaTeX notes and assessment synced through Git/Overleaf
- AI-assisted development and repository maintenance under human review
- one persistent development environment on the HPC

This creates a course that is easier to maintain, easier to adapt, and closer to how quantitative research is actually done.

Speaker notes:

End with the educational claim, not the tooling. The point is a course where students learn statistics as a living computational practice.

Time: 1 minute

---

# Optional 10-minute version

Use slides 1, 2, 3, 4, 6, 8, 9, 11, 12.

Suggested timing:

- opening and motivation: 2 minutes
- notebook/Colab design: 2 minutes
- course arc: 1 minute
- student workflow demo: 2 minutes
- AI/HPC/Git workflow: 2 minutes
- safeguards and conclusion: 1 minute

---

# Optional 20-minute version

Use all slides and include a short live demo.

Suggested timing:

- motivation and course design: 5 minutes
- course materials and student workflow: 5 minutes
- development workflow and AI: 6 minutes
- benefits, challenges, conclusion: 4 minutes

---

# Suggested live demo

Keep the demo to one notebook and one concept.

1. Open the repository README.
2. Click the Colab badge.
3. Open one lecture notebook.
4. Run a short simulation cell.
5. Change one parameter and rerun.
6. Show that the same material is version controlled in Git.

Good candidate notebooks:

- `Lectures/Lecture_03_PDM.ipynb`: distributions and confidence levels
- `Lectures/Lecture_06_PDM.ipynb`: outliers, model comparison, bootstrap
- `Lectures/Lecture_10_PDM.ipynb`: Monte Carlo and MCMC

---

# One-sentence summary

I developed the course as a reproducible computational learning environment: students can read, run, fork, and modify the lectures through Colab or a local VS Code/Git setup, while Git, Overleaf, the HPC, and AI-assisted editing and repository maintenance make the course maintainable and extensible.
