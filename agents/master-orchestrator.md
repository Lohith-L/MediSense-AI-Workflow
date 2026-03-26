# Master Orchestrator — MediSense AI

**Name:** `MediSense AI`

## Description
MediSense AI analyzes your medical report and delivers a personalized health summary, diet plan, and actionable guidance directly to your email — powered by Supervity.

## Step 1 — Input Form
```text
Step Type: Form / User Input
─────────────────────────────
Field 1:
  Name    : patient_email
  Type    : Email
  Label   : "Enter your email to receive your health report"
  Required: Yes

Field 2:
  Name    : medical_report
  Type    : File Upload (PDF)
  Label   : "Upload your medical report (PDF only)"
  Required: Yes
```

## Step 2 to 7 — Call Each Agent
```text
Step 2: Call Agent → Medical Data Extraction Workflow
  Input: {{medical_report}}

Step 3: Call Agent → Medical Lab Results Analyzer
  Input: {{step_2_output}}

Step 4: Call Agent → MediSense Research Agent
  Input: {{step_3_output}}

Step 5: Call Agent → MediSense Recommendation Agent
  Input: {{step_4_output}}

Step 6: Call Agent → MediSense Report Generator
  Input: {{step_5_output}}
  Also pass: {{patient_email}}

Step 7: Call Agent → MediSense Email Delivery Agent
  Input: {{step_6_output}}
  Also pass: {{patient_email}}
```

## Step 8 — Google Sheets Log
```text
Step Type : Google Sheets → Append Row
Sheet Name: MediSense AI — Patient Reports Log

Column A: {{current_timestamp}}
Column B: {{patient_email}}
Column C: {{report_type}}
Column D: {{health_score}}/100
Column E: {{abnormal_count}}
Column F: {{flagged_conditions}}
Column G: {{specialist_recommended}}
Column H: ✅ Report Sent Successfully
```

## Step 9 — Success Message
```text
Step Type: Show Message to User

Message:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✅ YOUR REPORT IS ON ITS WAY!
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🏥 MediSense AI has successfully analyzed 
   your medical report.

📧 Your personalized health report has been 
   sent to: {{patient_email}}

📄 Your report includes:
   ✓ Complete test analysis
   ✓ 7-day Indian diet plan  
   ✓ Exercise routine
   ✓ Doctor visit checklist
   ✓ Questions to ask your doctor

💚 Stay healthy!
   Team MediSense AI
   Powered by Supervity
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```
