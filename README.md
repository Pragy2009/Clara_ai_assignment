# Clara AI – Account Setup Automation

This project implements two automated pipelines in n8n that generate and maintain configuration files for a voice AI agent based on onboarding transcripts.

---

# Overview

The system automates the creation and updating of two key artifacts:

1. Account Memo – structured account configuration
2. Agent Specification – conversational agent setup

The pipelines process onboarding transcripts to generate structured outputs and maintain versioned updates.

---

# Pipelines

## Pipeline A – Initial Account Setup

Pipeline A processes onboarding transcripts and generates the initial configuration files.

Steps:
1. Read onboarding transcript
2. Extract structured information
3. Generate account memo
4. Generate agent specification
5. Save files to version v1

Output files:

outputs/accounts/demo_service_company/v1/

- account_memo.json
- agent_spec.json

---

## Pipeline B – Onboarding Updates

Pipeline B processes additional onboarding updates and applies them to the existing configuration.

Steps:
1. Load existing account memo
2. Extract update information
3. Merge updates
4. Regenerate agent specification
5. Produce changelog

Output files:

outputs/accounts/demo_service_company/v2/

- account_memo.json
- agent_spec.json
- changelog.json

---

# Folder Structure
clara-ai-assignment/
│
├── workflows/
├── dataset/
├── outputs/
├── screenshots/
└── README.md


---

# Technologies Used

- n8n (workflow automation)
- JSON data processing
- Local file system storage

---

# Example Outputs

Example files generated:

account_memo.json

agent_spec.json

changelog.json

---

# Future Improvements

Possible improvements include:

- LLM-based transcript parsing
- Automatic schema validation
- Integration with cloud storage
- API-based agent deployment

---

# Author

Pragy Jha

