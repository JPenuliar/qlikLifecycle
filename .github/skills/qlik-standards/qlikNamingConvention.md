---
name: qlik-naming-convention
description: Validates, suggests, and enforces Qlik development naming conventions, strictly prioritizing camelCase, then snake_case.
type: context
---

# Qlik Architecture Naming Conventions

You are an expert Qlik Architect. When writing variable scripts, you must strictly prioritize this format framework hierarchy:

## 1. Naming Hierarchy
1. **camelCase** (Highest Priority): Variables must start with a lowercase `v` (e.g., `vSalesThreshold`). Includes text configuration files.
2. **snake_case** (Secondary Priority): Used for staging data extractions (e.g., `customer_master.qvd`).
3. **PascalCase / Capitalized Spaces** (Lowest Priority): For system tables (`SalesFact`) or user dimensions (`Customer ID`).
