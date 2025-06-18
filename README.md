# Any_Chain
# 🏭 Production Line Process Overview

This project simulates an automated production line using **AnyLogic**, designed to handle both fragile and non-fragile products. The system showcases intelligent material handling, real-time quality checks, and robust failure management — making it suitable for educational or industrial simulation purposes.

---

## 🔄 Workflow

### 1. Input Stage
- Open boxes (raw materials) arrive on the production line.

### 2. Box Classification
- **Fragile Boxes**:
  - Rerouted via **Conveyor 2** to **Machine M1**.
  - Sealed and labeled as **"Fragile"**.

- **Non-Fragile Boxes**:
  - Sent directly via **Conveyor 3** to **Machine M2** for sealing.

### 3. Merge & Final Processing
- All sealed boxes (fragile and non-fragile) converge at **Machine M3** via **Conveyor 3**.
- **Machine M3** performs a **quality check**:
  - Boxes are categorized as **Conforming** or **Non-Conforming**.

---

## ⚠️ Failure Handling

In case of failure, especially a **Machine M1 breakdown**, the system applies one of three corrective decisions:

### 🔧 D1: Dual Processing with Machine M3
- The product passes through **Machine M1** as a **pass-through conveyor** (no processing delay).
- Then, it is processed on **Machine M3** with additional time compensation to cover the missed operation.
- Machine M1 is reconfigured as a conveyor from **Conveyor 1** to **Machine M3**.
- M1 processing time is removed; processing time is adjusted on M3.

### 🔁 D2: Redirect to Machine M2
- Type 1 products in the queue are **rerouted to Machine M2** if M1 fails.
- Machine M2 is reconfigured to handle the task with **updated processing time parameters**.

### ⏱️ D3: Prioritize Type 2 Production
- During M1 downtime, **Type 2 products** are prioritized.
- Type 1 products waiting in queue are **postponed** until M1 is repaired.
- Dynamic rescheduling ensures continuity for unaffected product types.

All failure events and corrective actions are logged in a dedicated database for traceability.

---

## ❗ Potential Issues

- **Machine M1 Failure**

- **Quality Defects**

 
---

## 📊 Performance Tracking

- **Inputs**:
  - Orders and machine parameters are imported from an **Excel file**.

- **Outputs**:
  - Key Performance Indicators (KPIs) are recorded in a structured **Excel log** for monitoring and analysis.

---

## 🛠️ Tools Used

- [AnyLogic](https://www.anylogic.com/) – For discrete event and agent-based simulation  
- Excel – For input/output data handling  

---





