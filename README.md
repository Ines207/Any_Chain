# Any_Chain
🏭 Production Line Process Overview

This project simulates an automated production line system designed to handle and process different types of boxes, including fragile ones. The system ensures quality, efficiency, and fault-tolerance through smart routing and real-time tracking.

🔄 Workflow

Input Stage

Open boxes arrive on the production line.

Box Classification

Fragile Boxes: Redirected via Conveyor 2 to Machine M1, where they are sealed and labeled "Fragile".

Non-Fragile Boxes: Sent directly via Conveyor 3 to Machine M2 for sealing.

Merging and Final Processing

All sealed boxes (fragile and non-fragile) are routed to Machine M3 via Conveyor 3.

Machine M3 performs a quality check:

Boxes are classified as Conforming or Non-Conforming.

⚠️ Failure Handling
If a problem is detected, the system initiates one or more of the following corrective actions:

Rerouting materials

Recalibrating machines

Triggering alerts and logging the issue in a dedicated database

❗ Potential Issues & Responses
Machine M1 Failure: Fragile box processing halts; fallback protocols are triggered to ensure traceability and minimize downtime.

Quality Defects: Automatically rejected and subjected to root-cause analysis.

📊 Performance Tracking
Inputs:

Orders and machine parameters are loaded from an Excel file.

Outputs:

Key Performance Indicators (KPIs) such as throughput, defect rates, and downtime are recorded to an Excel log.

Outputs: Key performance indicators (KPIs) are recorded in an Excel log.
