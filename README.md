# qlikLifecycle 🚀

Welcome to the **qlikLifecycle Knowledge Operating System (Knowledge OS)**. This repository serves as the centralized governance, automation, and asset framework layer for our end-to-end Qlik application development lifecycle.

By storing our development standards, reusable data conversion snippets, and active project challenges here, **GitHub Copilot** natively indexes this repository to act as a real-time architectural guardrail during code and chat sessions.

---

## 🛠️ The Knowledge OS Framework Architecture

This repository segregates system-level AI configurations and human intake forms from downstream scripting assets.

```text
qlikLifecycle/
│
├── .github/                           # GitHub System Configuration
│   ├── ISSUE_TEMPLATE/                # Automated Intake Infrastructure
│   │   └── knowledge-gap-form.yml     # GitHub Issue form to log new technical unknowns
│   │
│   └── skills/                        # Dedicated Copilot Custom Skills Directory
│       ├── qlik-standards/            
│       │   └── qlikNamingConvention.md # Naming standards driver (camelCase priority)
│       └── knowledge-gap/             
│           └── knowledgeGap.md        # Active structural unknown register
│
├── config/                            # Environment-level asset management
│   └── deploymentConfig.json          # Environment mapping, server paths, and variables
│
└── README.md                          # Repository System Map (This File)
```

---

## 📏 Core Style Guideline Hierarchy

All assets, variables, script files, and routines created inside this ecosystem must strictly adhere to the following priority hierarchy without exception:

1. **camelCase** (Highest Priority)
   - **Variables:** Environment, control, and expression hooks. Must begin with a lowercase `v` (e.g., `vCurrentYear`, `vSalesThreshold`).
   - **Subroutines:** Reusable custom script blocks (e.g., `subLoadDimensions`).
   - **Script Files:** Include text assets or code streams (e.g., `dataLoadScript.qvs`).
2. **snake_case** (Secondary Priority)
   - **Data Files:** Pure database target extractions or staging layers (e.g., `customer_master.qvd`).
3. **PascalCase & Capitalised Spaces** (Lowest Priority / Fallbacks)
   - **Data Model Tables:** Internal Qlik engine technical tables (e.g., `SalesFact`).
   - **UI Fields:** Columns exposed explicitly on analytics sheets for business users (e.g., `Customer ID`).

---

## 🤖 Interacting via GitHub Copilot Chat

Because this repository uses the Custom Skills engine, you can ground your AI chat sessions using your workspace context. Open your IDE or GitHub Chat interface and try these operational prompts:

* **To Review Names:** `@workspace /qlik-naming-convention check my load script for variable format violations.`
* **To Implement Conversions:** `@workspace /qlik-naming-convention write an expression to turn our ERP status text into a standard boolean flag.`
* **To Query Project Unknowns:** `@workspace /knowledge-gap are there any active roadblocks involving timezones or currency fields?`

---

## 📥 Ingestion Pipeline (Logging a Knowledge Gap)

Never update `knowledgeGap.md` manually. To log an unexpected architectural hurdle, missing schema definition, or transformation blocker:
1. Navigate to the **Issues** tab of this repository.
2. Click **New Issue** and choose **Reporting a Qlik Knowledge Gap**.
3. Complete the form. The background GitHub Actions worker will automatically parse, clean, format, and append the gap to our live AI context file.
