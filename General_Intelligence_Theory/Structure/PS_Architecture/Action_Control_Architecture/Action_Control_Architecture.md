# ACTION CONTROL STRATEGIES (Micro-Layer)
(For ONE execution of the Canonical Action Architecture)

1️⃣ Sequential Action Mode (default)
Run nodes in order from Context → Transfer Plan.

2️⃣ Micro-Parallel Mode (only where it reduces latency)
Allow parallel execution of:
- Evidence Base ↔ Uncertainty Map
- Alternatives Considered ↔ Risk Awareness
- Instrumentation ↔ Validation planning
(Everything else remains sequential)

3️⃣ Micro-Skip Rule
Skip a node IF its output already exists and is trusted.
Examples:
- Skip Stakeholders if already fixed for this phase
- Skip Alternatives if strategy is mandated
- Skip Algorithm if non-algorithmic task

4️⃣ Micro-Loop Rule (local iteration)
If Validation/Feedback fails:
- Loop back to the nearest upstream cause:
  - If procedure wrong → Procedure / Technique
  - If tool mismatch → Toolset / Strategy
  - If assumptions wrong → Assumptions / Evidence / Uncertainty
(Do NOT jump across PS phases here; PS handles macro jumps)

5️⃣ Early Validation Rule
Inject small validation checks during:
- Modeling inside Action (if building representations)
- Procedure execution (after each major step)
This prevents late failure.

6️⃣ Decision Gate Rule
Decision Gate outputs one of:
- Continue (next node)
- Revise (loop locally)
- Pivot (change Strategy/Toolset)
- Escalate-to-PS (signal PS controller to jump phases)

7️⃣ Recursion Rule (Sub-action)
If a step becomes a subproblem with its own goal + constraints:
spawn a nested Action run (or nested PS run if big),
then return the artifact to the parent Action at Procedure/Tool level.
