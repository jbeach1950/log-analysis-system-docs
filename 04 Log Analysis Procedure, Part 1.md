********************************************************************************
# Document 04 -- Log Analysis Procedure, Part 1 (Threat Detection & Filtering)
Rev 1.0.0 - Original Issue
********************************************************************************

---

## Pre-Execution Context

- [cite_start]This document (Part 1) begins execution at **STEP 1 OF 31 (Section 1, Step 1.1)**[cite: 04].
- [cite_start]Execution commences only after the pre-execution sequence defined in **Document 10 – Read Me** is completed and Mandatory Pauses 1 and 2 are resolved[cite: 04, 10].
- [cite_start]The AI automatically proceeds to **Phase 2 – Log Analysis, Part 1 (this document)** at **STEP 1 OF 31**, unless the user has explicitly instructed termination[cite: 04, 10].

---

## Core Principles

- [cite_start]**100% Consistency in Critical Outcomes**: All steps in this procedure must ensure **unanimous agreement** among the 6 AIs on **identifying threats** (e.g., suspicious IPs, request patterns, review cycles)[cite: 01, 04].  
  - [cite_start]Example: If Step 2.3 identifies `34.74.248.16` as a threat, all 6 AIs must confirm the IP is **malicious**[cite: 04].

- **90%-10% Rule for Interpretation/Description**:
  - [cite_start]**90% Agreement**: All 6 AIs must align on the **existence and nature** of each threat (e.g., brute-forcing, scanning)[cite: 01, 04].  
  - [cite_start]**10% Flexibility**: Minor variations in **description or contextual wording** are permitted, provided they do not alter the threat’s classification or inclusion in the final set of flagged entities[cite: 04].  
  - [cite_start]Example: One AI may describe a threat as *“high-risk brute-forcing”* while another says *“aggressive credential-scanning”*, with identical classification and handling[cite: 04].

- [cite_start]**6-AI Collaboration Framework**: Any proposed procedural change that introduces **divergence beyond the 10% boundary**, or that changes critical outcomes, must be **flagged for collaborative review** by all 6 AIs[cite: 01, 04].  
  - [cite_start]Unanimous agreement under **Document 02 – How to Revise Log Analysis Procedure** is required to implement the change[cite: 01, 02].

---

## Procedural Steps

### Section 1: Initialization & Orientation

**STEP 1 OF 31**
Phase 2 – Section 1 – Document 04 – Step 1.1 – Next Mandatory Pause: 3
- [cite_start]**1.1 Structural Matrix and Procedural Scope**: Display the structural matrix and announce the procedural scope for the run[cite: 04, 10].

**STEP 2 OF 31**
Phase 2 – Section 1 – Document 04 – Step 1.2 – Next Mandatory Pause: 3
- [cite_start]**1.2 Data Receipt Confirmation**: Acknowledge receipt of all 11 documentation files and the log data file(s)[cite: 04, 10].

**STEP 3 OF 31**
Phase 2 – Section 1 – Document 04 – Step 1.3 – Next Mandatory Pause: 3
- [cite_start]**1.3 Await Authorization**: Await explicit user authorization to begin the analysis[cite: 04].

[cite_start]**Mandatory Pause after Step 1.3** (Mandatory Pause 3) 

---

### Section 2: Log Filtering Protocol

**STEP 4 OF 31**
Phase 2 – Section 2 – Document 04 – Step 2.1 – Next Mandatory Pause: 4
- [cite_start]**2.1 Administrative Exclusion**: Immediately identify and remove all log entries originating from the designated Administrator IP(s) (e.g., `172.83.66.67`)[cite: 04]. [cite_start]These entries are excluded from all subsequent analysis to preserve system resources[cite: 04].

**STEP 5 OF 31**
Phase 2 – Section 2 – Document 04 – Step 2.2 – Next Mandatory Pause: 4
- [cite_start]**2.2 Validate Structural Integrity**: Validate the structural integrity of all remaining log entries (Apache Combined Log Format)[cite: 04].

**STEP 6 OF 31**
Phase 2 – Section 2 – Document 04 – Step 2.3 – Next Mandatory Pause: 4
- [cite_start]**2.3 Detect and Filter Malicious Patterns**: Scan for exploit attempts, credential harvesting, and vulnerability probes (e.g., Response Splitting, Shadow AI probes)[cite: 04].

**STEP 7 OF 31**
Phase 2 – Section 2 – Document 04 – Step 2.4 – Next Mandatory Pause: 4
- [cite_start]**2.4 Classify and Segregate Automated Bots**: Identify legitimate crawlers vs. suspicious harvesters using temporal analysis, resolution validation, and **Frozen Environment Detection**[cite: 04, 10].
- [cite_start]**Synchronous Burst Automation Marker**: Any set of two or more identical requests occurring at **exactly the same timestamp** must be classified as automated traffic[cite: 04, 10].

**STEP 8 OF 31**
Phase 2 – Section 2 – Document 04 – Step 2.5 – Next Mandatory Pause: 4
- [cite_start]**2.5 Audit Rule-Based Blocks**: Document log entries successfully blocked by **Document 07 (htaccess.md)**[cite: 03, 04].

**STEP 9 OF 31**
Phase 2 – Section 2 – Document 04 – Step 2.6 – Next Mandatory Pause: 4
- [cite_start]**2.6 Deduplicate Entries**: Remove duplicate entries to prevent inflated counts[cite: 04].

**STEP 10 OF 31**
Phase 2 – Section 2 – Document 04 – Step 2.7 – Next Mandatory Pause: 4
- [cite_start]**2.7 Session Mapping & Reconciliation**: Aggregate entries into sessions using unique **IP Address + User-Agent** and a **30-minute inactivity window**[cite: 04, 10]. [cite_start]Confirm final session counts[cite: 04].

#### Section 2 Funnel Metrics (Mandatory Output at Pause)
- [cite_start]Total raw log entries in scope[cite: 04].
- [cite_start]Entries removed via Administrative Exclusion (Step 2.1)[cite: 04].
- [cite_start]Entries removed as malicious/exploit traffic[cite: 04].
- [cite_start]Entries removed as legitimate bots[cite: 04].
- [cite_start]Entries removed as automated scanners[cite: 04].
- [cite_start]Entries removed as duplicates[cite: 04].
- [cite_start]**Remaining validated entries (pre-mapping count)**[cite: 04].
- [cite_start]**Total session count (post-mapping count)**[cite: 04].

[cite_start]**Mandatory Pause after Step 2.7** (Mandatory Pause 4) 

---

********************************************************************************
End of Document 04 -- Log Analysis Procedure, Part 1 (Threat Detection & Filtering)
This file is complete and has not been truncated.
********************************************************************************