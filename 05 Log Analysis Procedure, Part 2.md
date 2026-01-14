********************************************************************************
# Document 05 -- Log Analysis Procedure, Part 2 (Session Definitions & Security)
Rev 1.0.0 - Original Issue
********************************************************************************

---

## Pre-Execution Context

- This document (Part 2) begins execution at **STEP 11 OF 31 (Section 3, Step 3.1)**.
- It follows the successful completion of **Document 04 (Part 1)** and the resolution of Mandatory Pause 4.
- The AI automatically proceeds to **Phase 3 – Log Analysis, Part 2 (this document)** unless the user has explicitly instructed termination.

---

## Core Principles

- **100% Consistency in Critical Outcomes**: All steps in this procedure must ensure **unanimous agreement** among the 6 AIs on the **classification of sessions** and the **identification of security trends**.  
  - Example: If Step 3.2 identifies a session as a "High-Risk Prober," all 6 AIs must confirm this classification.

- **90%-10% Rule for Interpretation/Description**:
  - **90% Agreement**: All 6 AIs must align on the **existence and nature** of session behaviors (e.g., path traversal, resource exhaustion).  
  - **10% Flexibility**: Minor variations in **descriptive terminology** are permitted, provided the underlying security classification and count remain identical.  
  - Example: One AI may describe a session as *"repetitive asset-probing"* while another uses *"sequential resource-scanning"*, with identical session counts.

- **6-AI Collaboration Framework**: Any proposed procedural change that introduces **divergence beyond the 10% boundary**, or that changes critical outcomes, must be **flagged for collaborative review**.  
  - Unanimous agreement under **Document 02** is required to implement the change.

---

## Procedural Steps

### Section 3: Session Contextualization & Classification

**STEP 11 OF 31**
Phase 3 – Section 3 – Document 05 – Step 3.1 – Next Mandatory Pause: 5
- **3.1 Identify Primary Landing Paths**: Map all sessions to their initial entry point (e.g., `/`, `/index.html`, or direct deep-links).

**STEP 12 OF 31**
Phase 3 – Section 3 – Document 05 – Step 3.2 – Next Mandatory Pause: 5
- **3.2 Classify Behavioral Context**: Analyze session progression (referrers, request sequences) to distinguish between benign navigation and suspicious probing.

**STEP 13 OF 31**
Phase 3 – Section 3 – Document 05 – Step 3.3 – Next Mandatory Pause: 5
- **3.3 Separate Human Candidates**: Filter sessions that lack automated markers (from Section 2) for further human-centric behavioral analysis.

**STEP 14 OF 31**
Phase 3 – Section 3 – Document 05 – Step 3.4 – Next Mandatory Pause: 5
- **3.4 Audit Resource Access**: Identify sessions targeting sensitive files or unauthorized directories (e.g., `.env`, `.git`, `/admin`).

#### Section 3 Funnel Metrics (Mandatory Output at Pause)
- Total sessions entering Section 3.
- Sessions classified as legitimate human candidates.
- Sessions classified as high-risk automated/malicious probes.
- Sessions targeting unauthorized assets.

**Mandatory Pause after Step 3.4** (Mandatory Pause 5)

---

### Section 4: Trend Analysis & Security Correlation

**STEP 15 OF 31**
Phase 3 – Section 4 – Document 05 – Step 4.1 – Next Mandatory Pause: 6
- **4.1 Correlate IP Intelligence**: Cross-reference high-risk sessions with known hostile ranges and previous run identifications.

**STEP 16 OF 31**
Phase 3 – Section 4 – Document 05 – Step 4.2 – Next Mandatory Pause: 6
- **4.2 Identify Temporal Spikes**: Detect bursts in traffic that suggest coordinated attacks or distributed scans.

**STEP 17 OF 31**
Phase 3 – Section 4 – Document 05 – Step 4.3 – Next Mandatory Pause: 6
- **4.3 Detect Persistent Threats**: Identify IPs or ranges that appear across multiple days/log files with hostile intent.

**STEP 18 OF 31**
Phase 3 – Section 4 – Document 05 – Step 4.4 – Next Mandatory Pause: 6
- **4.4 Propose Immediate Blocks**: Generate a list of IPs recommended for immediate blocking via **Document 07 (.htaccess)**.

#### Section 4 Funnel Metrics (Mandatory Output at Pause)
- New persistent threats identified.
- Total IPs recommended for blocking.
- Summary of high-risk trends.

**Mandatory Pause after Step 18 OF 31** (Mandatory Pause 6)

---

********************************************************************************
End of Document 05 -- Log Analysis Procedure, Part 2 (Session Definitions & Security)
This file is complete and has not been truncated.
********************************************************************************