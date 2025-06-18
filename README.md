# Any_Chain
Production Line Process Overview
This system processes raw materials (open boxes), some of which are fragile, and transforms them into finished products through a series of automated steps.

Workflow
Input: Open boxes arrive on the production line.

Fragile boxes are redirected via Conveyor 2 to Machine M1, where they are sealed and labeled "Fragile".

Non-fragile boxes move directly via Conveyor 3 to Machine M2 for sealing.

Merge & Final Processing:

Both sealed box types converge at Machine M3 via Conveyor 3.

A quality check categorizes them as Conforming or Non-Conforming.

Failure Handling
If issues arise, the system executes 3 corrective actions  and logs them in a database.

Potential Issues
Machine M1 Failure: Production halts for fragile boxes; fallback protocols activate.

Quality Defects: Automated rejection and root-cause analysis.

Performance Tracking
Inputs: Orders and machine parameters are read from an Excel file.

Outputs: Key performance indicators (KPIs) are recorded in an Excel log.
