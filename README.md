# qlikLifecycle 🚀

Welcome to **qlikLifecycle**, the decentralized Knowledge Operating System (Knowledge OS) governing our end-to-end Qlik application development pipeline. 

This repository functions as a programmable context layer. By maintaining our development standards, reusable data conversion snippets, and active project roadblocks here, **GitHub Copilot** natively indexes this workspace to enforce architectural guardrails during code and chat sessions.

---

## 📏 Naming Convention Hierarchy

To ensure code consistency across all development tiers (Extract, Transform, Presentation), all variables, script files, and routines must strictly adhere to this priority framework without exception:

1. **camelCase** (Highest Priority)
   - **Variables:** All script, environment, control, and UI variables. Must begin with a lowercase `v` (e.g., `vCurrentYear`, `vSalesThreshold`).
   - **Subroutines:** Custom reusable macro logic Blocks (e.g., `subLoadDimensions`).
   - **Script Files:** Configuration assets and file includes (e.g., `dataLoadScript.qvs`).
2. **snake_case** (Secondary Priority)
   - **Data Files:** Target database extract streams and raw storage layers (e.g., `customer_master.qvd`).
3. **PascalCase & Capitalized Spaces** (Lowest Priority / Fallbacks)
   - **Data Model Tables:** Internal Qlik engine technical table groupings (e.g., `SalesFact`).
   - **UI Fields:** Columns exposed directly on visual sheets for business end-users (e.g., `Customer ID`).

---

## 📂 Repository System Architecture

The repository isolates system-level AI workflows and intake forms from production configuration files:

```text
qlikLifecycle/
│
├── .github/                           # GitHub System Configurations
│   ├── ISSUE_TEMPLATE/                # Custom Intake Infrastructure
│   │   └── knowledge-gap-form.yml     # Live: Structured form for logging unknowns
│   │
│   ├── workflows/                     # Automated System Processes
│   │   └── updateKnowledgeGap.yml     # Live: Background worker pipeline script
│   │
│   └── skills/                        # Dedicated Copilot Custom Skills
│       ├── qlik-standards/            
│       │   └── qlikNamingConvention.md # Prompt driver enforcing camelCase standards
│       └── knowledge-gap/             
│           └── knowledgeGap.md        # Plaintext memory register of pipeline blockers
│
└── config/                            # Runtime Production Assets
    └── qlikDataConversions.qvs        # Executable global script include macro library
```

---

## 📥 Live Ingestion: Logging a Knowledge Gap

Do not modify the `knowledgeGap.md` file manually. To log an active technical hurdle, unmapped data schema, or upstream data pipeline block:
1. Navigate to the **Issues** tab of this repository.
2. Click **New Issue** and choose **Reporting a Qlik Knowledge Gap**.
3. Complete the custom structured fields and submit.
4. The **GitHub Actions background runner** will automatically parse the payload, format it into standardized markdown, and append it to our active AI context database.

---

## 🤖 Copilot Chat Prompts for the Team

Because our workspace context is hooked directly into the Copilot engine, developers can use these exact commands in their IDE or GitHub Chat interface to ground their daily workflows:

* **Review Variable Layouts:**
  > `@workspace /qlik-naming-convention check my load script for variable naming violations.`
* **Generate Standards-Compliant Code:**
  > `@workspace /qlik-naming-convention write an expression to convert an alphanumeric ERP flag into a standard binary boolean.`
* **Audit Outstanding Pipeline Risks:**
  > `@workspace check our active knowledge-gap records before I write this extract script.`
