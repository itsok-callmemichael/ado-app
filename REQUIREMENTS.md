# ADO App - Assignment Despite Objection Digital Form

## Overview
A mobile-friendly web app that digitizes the CNA/NNU "Assignment Despite Objection" (ADO) paper form used by nurses when they have unsafe assignments. The app must mirror the paper form exactly.

## Tech Stack
- Single-page HTML/CSS/JS web app (no framework needed, keep it simple)
- Mobile-first responsive design
- Signature pad library (signature_pad.js from CDN)
- PDF generation (jsPDF + html2canvas or jsPDF alone)
- No backend needed - runs entirely in browser

## Design
- Clean, professional, mobile-friendly
- CNA colors: Red (#CC0000) and white, with dark accents
- Large touch targets for checkboxes and buttons
- Two tabs: "ADO Form" and "Instructions"

## Form Structure (mirror the paper form EXACTLY)

### Header
- Title: "CALIFORNIA - Assignment Despite Objection/OutPatient"
- Subtitle: "California Nurses Association / National Nurses United"
- Introductory text: "You must first verbally protest your assignment to your supervisor at the time you believe it is unsafe. This is usually at the start of the shift, but might occur at any time. If your supervisor does not make a satisfactory adjustment to the assignment, complete this form to the best of your knowledge and distribute the ADO copies according to the instructions on the reverse side."

### SECTION I
- Label: "I/We" with a text input for nurse name
- "Add Nurse" button - clicking adds another name input field. Each added nurse gets a signature area at the bottom of the form.
- "Registered nurse(s) employed at" with fields for: Facility, Unit/Dept, Shift
- "Hereby protest my/our assignment as:" with checkboxes:
  - Telephone Advice RN, Nurse Practitioner, OutPatient OR RN, Station RN, Injection RN, Recovery Room RN, Charge RN/Team Leader RN, Emergency Dept. RN, Operating Room RN, Other RN (with text input)
- "given to me/us by" with fields for: Name/Title, Date, Time
- Legal paragraph about California Nursing Practice Act

### SECTION II - Action
- Supervisor notified (text) + Date/Time
- Supervisory response (textarea)
- Other person notified (text) + Date/Time
- Other person's response (textarea)

### SECTION IIIa - Objection Grounds (check all that apply)
- All checkboxes with nested sub-checkboxes as on the form
- See REQUIREMENTS_DETAIL.md for exact checkbox text

### SECTION IIIb - Working conditions
- Meal period missed? Yes/No
- Break missed? Yes/No
- Overtime worked? Yes/No

### SECTION IV - Type of unit
- Type of unit, Patient classification system name, Census, Acuity (Low/Med/High/Extreme radio), Staffing system variance

### SECTION V - Patient care staffing count
- Number of RNs, LVNs, MAs, Aides (number inputs)
- Clerk? Yes/No, Lift team? Yes/No, Transport? Yes/No

### SECTION VI - Brief Problem Statement (large textarea)

### SECTION VII - Patient care affected (large textarea)

### Signature Section
- For each nurse in Section I: name displayed, signature canvas pad, Clear button, auto date/time stamp on sign

### Actions
- Generate PDF button, Clear Form button (with confirmation)

## Instructions Tab
Include all instruction text, Title 22, Title 16 provisions, and CNA/NNU office addresses (Oakland, Sacramento, San Jose, Fresno, Los Angeles, San Diego).
