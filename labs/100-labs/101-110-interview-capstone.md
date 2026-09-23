# Labs 101-110 — Interview and Expert Challenges

## Lab 101 — Explain the four Git areas
**Objective:** Teach working tree, index, local repository, and remote repository. **Task:** Demonstrate one file moving through each state. **Expected:** Clear mental model. **Challenge:** Explain where HEAD fits. **Solution:** Draw the state transitions. **Interview:** Why does staging exist?

## Lab 102 — Explain Git objects
**Objective:** Demonstrate blob/tree/commit relationships. **Commands:** `git cat-file -p HEAD`, inspect its tree, then a blob. **Expected:** Object graph is understandable. **Challenge:** Compare object ID changes after editing. **Solution:** Content changes produce different object IDs. **Interview:** What does a commit point to?

## Lab 103 — Explain reset modes
**Objective:** Distinguish soft, mixed, and hard reset. **Task:** Create a disposable repo and demonstrate each. **Expected:** You can identify changes left in working tree/index. **Challenge:** Recover after hard reset using reflog. **Solution:** Practice only in a temporary repo. **Interview:** What does `git reset --mixed` move?

## Lab 104 — Explain revert
**Objective:** Demonstrate safe undo of published history. **Task:** Create a commit, publish it in a practice branch, then `git revert`. **Expected:** A new inverse commit appears. **Challenge:** Revert a merge in a controlled repository. **Solution:** Inspect parent structure before selecting the mainline. **Interview:** Why does revert preserve history?

## Lab 105 — Diagnose a merge conflict verbally
**Objective:** Practice interview communication. **Scenario:** Two branches changed the same lines. **Task:** Explain detection, conflict markers, resolution, staging, and continuation. **Expected:** Complete and ordered explanation. **Challenge:** Include abort path. **Solution:** State what Git can and cannot decide automatically. **Interview:** How do you resolve a conflict?

## Lab 106 — Design a branching strategy
**Objective:** Select a branching model for a small team. **Task:** Compare trunk-based development, short-lived feature branches, and release branches. **Expected:** Documented trade-offs tied to team needs. **Challenge:** Add hotfix handling. **Solution:** Choose based on release cadence, review controls, and operational needs. **Interview:** What branching strategy have you used and why?

## Lab 107 — Debug a rejected push
**Objective:** Diagnose non-fast-forward errors. **Task:** Reproduce with two clones and document the exact recovery commands. **Expected:** No destructive overwrite. **Challenge:** Add a force-with-lease scenario on a private branch. **Solution:** Fetch, inspect, integrate, then push. **Interview:** What does non-fast-forward mean?

## Lab 108 — Review a malicious-looking workflow
**Objective:** Practice security review. **Task:** Inspect triggers, permissions, secrets, untrusted inputs, and third-party actions. **Expected:** Concrete findings tied to specific lines/behaviors. **Challenge:** Redesign with read-only permissions and safer triggers. **Solution:** Minimize privilege and isolate untrusted code. **Interview:** What can a compromised runner expose?

## Lab 109 — Build a teaching demo
**Objective:** Explain Git visually. **Task:** Create a five-minute demo showing status → add → commit → branch → merge → log graph. **Expected:** Students can predict each state transition. **Challenge:** Insert a deliberate conflict. **Solution:** Narrate state before every command. **Interview:** Why teach concepts before memorizing commands?

## Lab 110 — Final instructor challenge
**Objective:** Create an original Git/GitHub exercise. **Task:** Design a lab with objective, scenario, setup, commands, expected output, challenge, solution, and interview questions. **Expected:** A reusable classroom lab. **Challenge:** Include one recovery or security scenario. **Solution:** Ensure the exercise is deterministic and safe to run. **Interview:** Defend your lab design choices.