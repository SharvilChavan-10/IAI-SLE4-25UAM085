AI Contribution Log — SLE-4

Student Details

- Name: Sharvil S. Chavan
- PRN: 25UAM085
- Division: B
- Course: 02AML204 — Introduction to Artificial Intelligence
- Project: Maze Solver System — Architecture Decision Record (ADR)
- AI Tool Used: Claude
- GitHub Profile: https://github.com/SharvilChavan-10

---

1. Purpose of Using AI

Claude was used as an assistance tool while preparing the SLE-4 Architecture Decision Record. It helped organize the report according to the ADR format, improve the clarity of explanations, calculate comparison ratios, and prepare viva questions.

The final architecture decision was to use Breadth-First Search (BFS) as the primary maze-solving algorithm, based on the profiling results from SLE-2 and the system architecture documented in SLE-3.

2. AI Contribution Details

Sr. No.| Task| AI Contribution| My Contribution
1| ADR structure| Helped organize the report into Context, Decision, Alternatives, Rationale, and Consequences.| Reviewed and finalized the report structure.
2| Context and decision| Helped draft explanations of the maze-solving problem and algorithm selection.| Confirmed that BFS would be the primary algorithm.
3| Performance analysis| Helped calculate and explain BFS-versus-DFS path-length ratios.| Checked the values against my SLE-2 profiling report.
4| Alternative algorithms| Helped organize the discussion of DFS, A*, and Greedy Best-First Search.| Reviewed the alternatives and their relevance to the project.
5| Architecture documentation| Helped explain the Frontier, Visited Set, Parent Map, and Neighbour Generator.| Verified the component names against my SLE-3 documentation.
6| Viva preparation| Suggested possible viva questions and concise answers.| Reviewed the questions and prepared to explain the project.

3. Performance Data Verification

The following values were used in the ADR and checked against my SLE-2 report.

Maze Size| BFS Path Length| DFS Path Length
20×20| 39 cells| 79 cells
40×40| 79 cells| 193 cells
70×70| 141 cells| 379 cells

These results supported the decision to select BFS because it produced shorter paths in the tested unweighted mazes, although DFS was faster in the experiments.

4. Example Prompts Used

The following are representative prompts describing the assistance required during report preparation. They are not intended to be a verbatim history of the AI conversation.

1. Help organize an Architecture Decision Record for a maze-solving system comparing BFS and DFS.
2. Explain the advantages, disadvantages, and trade-offs of selecting BFS as the primary algorithm.
3. Calculate and explain the path-length ratios using the profiling results from SLE-2.
4. Help explain the roles of the Frontier, Visited Set, Parent Map, and Neighbour Generator.
5. Suggest viva questions and answers based on the architecture decision.

5. Human Verification and Responsibility

I reviewed the AI-assisted content and checked the reported performance values against my earlier SLE work. I also checked the architecture terminology against my SLE-3 documentation.

I selected BFS as the primary algorithm based on the project's requirement for shortest-path quality. I am responsible for the final decision, the accuracy of the submitted report, and my understanding of the project.

AI assistance was used for drafting, organization, explanation, and analysis support. It does not replace my responsibility for understanding and defending the submitted work.

6. Conclusion

Using Claude helped me organize my SLE-4 report and prepare for the viva. The exercise improved my understanding of architecture decision-making, algorithm trade-offs, performance evaluation, and transparent AI-assisted development.

---

Declaration: This log records the AI assistance described in my SLE-4 report. Any additional prompts, code generation, or AI contributions should be documented if applicable.

Student: Sharvil S. Chavan

PRN: 25UAM085

Course: 02AML204 — Introduction to Artificial Intelligence
