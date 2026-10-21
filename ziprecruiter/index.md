---
layout: default
title: ZipRecruiter Proposal
nav_order: 3
---

# 📋 Product Proposal: Multi-Resume Management & Target Apply
**Platform:** ZipRecruiter Candidate Ecosystem | **Role:** Product Owner (Portfolio Initiative)
**Status:** MVP Scope Defined

---

## 1. Executive Summary & Objective
ZipRecruiter’s core value proposition is the **"1-Click Apply"** mechanism. However, the platform currently restricts candidates to hosting exactly **one active resume** at a time. In the modern job market, candidates heavily tailor their resumes to distinct roles.

> **The Problem:** Users must manually overwrite their single resume profile whenever applying to a different job type. This breaks the friction-free "1-Click" experience and risks sending the wrong resume to automated recruiter pipelines.
{: .note }
>
> **The Objective:** Enable job seekers to upload, label, and manage up to three (3) distinct resumes simultaneously and seamlessly select the optimal version during the 1-Click Apply flow.

---

## 2. Strategic Context and Why?

### User Persona & Friction Loop
* **Persona:** The Multi-Hyphenate Job Seeker *(e.g., someone applying to both Product Owner and Scrum Master positions)*.
* **Current UX Loophole:** User applies to Job A (Product) ➔ User goes to settings to upload Resume B (Scrum) ➔ User applies to Job B ➔ User realizes their active profile resume for Job A has now been retroactively updated/swapped in some historical views.

### Business Impact & Value

[Tailored Resumes] ➔ [Higher Recruiter Match Quality] ➔ [More Placements] ➔ [Increased Premium Revenue]

* **For the User:** Higher response rates due to highly relevant, targeted resume submissions.
* **For the Recruiter:** Drastically reduced "resume spam." Recruiters see keywords which match their job descriptions, increasing their satisfaction with ZipRecruiter's candidate matching algorithm.

---

## 3. Scope & Feature Prioritization (RICE Framework)
To ensure a lean, iterative release, features are prioritized using a simplified RICE matrix:

| Feature Item | Reach | Impact | Confidence | Effort | Priority |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Profile Resume Manager:** Upload up to 3 files, delete, and set a default "Primary" resume. | High | High | High | Med | **MVP (Must)** |
| **1-Click Apply Dropdown:** Inline toggle to select alternate resume before submission confirmation. | High | High | High | Med | **MVP (Must)** |
| **Smart Naming/Labeling:** Automatically parse and label resumes *(e.g., "Software Engineer vs Product")*. | Med | Med | Med | High | **V2 (Should)** |
| **In-App AI Tailoring Advice:** Feedback on which resume matches the target job description best. | High | Med | Low | High | **Future (Could)** |

---

## 4. Functional Requirements & User Stories

### 📦 Epic: Profile Resume Management 
> **User Story:** *As a job seeker, I want to upload and save multiple resumes in my profile settings, so that I don't have to keep re-uploading documents from my hard drive.*

#### Acceptance Criteria (Given-When-Then):
* **Given** a user is on the 'Profile Settings' page,
  * **When** they click the "Upload Resume" CTA,
  * **Then** they can add a file if their current total is less than 3.
  * **And** they must be prompted to assign a nickname/label to the file.
* **Given** a user has multiple resumes uploaded,
  * **When** they view the list,
  * **Then** one must be clearly badged as the "Primary Default" resume.

### ⏩ Epic 2: Tailored “One-Click Apply”
> **User Story:** *As a job seeker for a specific candidate role, I want to be able to choose which of my uploaded resumes to use when applying via the “1-Click Apply” action so that my application remains highly targeted.*

#### Acceptance Criteria (Given-When-Then):
* **Given** a user clicks the "1-Click Apply" CTA,
  * **When** they have more than one resume uploaded,
  * **Then** they are prompted to choose which resume to utilize via a micro modal,
  * **And** the "Primary Default" resume must be pre-selected.
* **When** they select an alternate resume and hit "Submit Application",
  * **Then** that specific resume on file is transmitted to the recruiter without changing the global "Primary Default" settings on their profile.

---

## 5. Technical Design and Wireframes

```text
🖼️ [Wireframe 1: Profile Settings Page Layout]
Showing the new slot structure accommodating 3 file blocks instead of 1.
```

```text
🖼️ [Wireframe 2: The 1-Click Dropdown]
Showing how the quick-apply button expands safely to let users tap their preferred resume file.
```

---

## 6. Success Metrics & Analytics (KPIs)
* **Feature adoption:** % of Monthly Active Users (MAU) holding >1 resume file.
* **Funnel Conversion:** Change in the completion rate of applications when a user triggers a 1-Click Apply action *(ensuring the resume choice dropdown doesn't introduce drop-off friction)*.
* **Recruiter Quality Index:** % of applications marked as "Thumbs Up" / "Qualified" by recruiters using the multi-resume application flow versus the legacy single-resume cohort.
