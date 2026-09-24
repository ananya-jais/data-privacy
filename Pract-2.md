------------------------------
## Practical 2: Privacy Impact Assessment (PIA)
Objective: To conduct a Privacy Impact Assessment (PIA) on a proposed or newly deployed technology system, identify potential privacy risks associated with processing user data, and design effective mitigation strategies.
------------------------------
## 1. Project / Technology Description

* Target Technology: AI-Driven Smart Attendance System using Facial Recognition (Proposed for a college campus or workspace).
* System Overview: The system utilizes high-definition cameras placed at entry and exit points. An AI algorithm scans individuals, matches their biometric facial data against a pre-registered database, and automatically marks their daily attendance.

------------------------------
## 2. Data Lifecycle Mapping
To evaluate privacy risks, we must track the movement of Personally Identifiable Information (PII) and biometric data across four key stages:

[Collection] ──> [Processing] ──> [Storage] ──> [Retention & Deletion]
   Camera           AI Vector       Central          Purged after
   Capture          Extraction      Database          Graduation


* Collection: Capturing live facial images, Student/Employee IDs, and timestamps.
* Processing: Converting facial images into mathematical coordinate matrices (facial templates).
* Storage: Storing the processed templates in a secure local or cloud-based server.
* Retention: Keeping the records for the duration of the academic year or employment tenure.

------------------------------
## 3. Privacy Risk Identification & Assessment Matrix

| Privacy Risk Area | Identified Vulnerability / Risk | Risk Level (High/Med/Low) |
|---|---|---|
| Biometric Identity Theft | If the central database is breached, permanent biometric data (facial structures) could be leaked. Unlike a password, a face cannot be changed. | High |
| Function Creep | The attendance cameras might be repurposed for continuous campus surveillance, tracking social groups or student movement without consent. | Medium |
| Lack of Informed Consent | Students or visitors might have their faces scanned automatically upon entry without explicit awareness or choice. | Medium |
| Data Retention Overstay | Biometric data remaining active indefinitely on servers long after a student has graduated or left the institution. | Medium |

------------------------------
## 4. Risk Mitigation Strategies (Privacy by Design)
To make the system compliant with modern privacy frameworks (such as India's DPDP Act 2023 or GDPR), the following measures must be built into the system:

* Mitigation for Biometric Theft (One-Way Hashing):
* Strategy: The raw image must be instantly deleted after processing. The system must only store mathematical facial coordinates as an encrypted one-way hash. If data is leaked, hackers cannot reverse the hash back into a human face image.
* Mitigation for Function Creep (Strict Purpose Limitation):
* Strategy: Programmatic controls must isolate the data. The attendance data feed must not be linked to any other campus system (like library access, cafeteria billing, or security CCTV monitoring).
* Mitigation for Consent & Transparency (Notice & Opt-Out Options):
* Strategy: Clear physical signboards must be posted at entry points. Furthermore, an alternative manual mechanism (like a digital ID card tap) must be provided for individuals who opt out of facial recognition.
* Mitigation for Retention Risk (Automated Purge Script):
* Strategy: Set a hard-coded data lifecycle rule. A student’s biometric data profile must be completely wiped from all server backups within 30 days of graduation or termination of enrollment.

------------------------------
## 5. Conclusion
Conducting this Privacy Impact Assessment ensures that the institution does not deploy a blind mass-surveillance tool. By integrating Privacy by Design (PbD) principles, the AI Attendance System achieves its goal of administrative efficiency while safeguarding the fundamental privacy rights of the campus community.
------------------------------

