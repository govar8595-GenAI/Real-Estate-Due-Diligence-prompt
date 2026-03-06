🏠 Real Estate Due Diligence Brief — AI Prompt System

> A production-ready prompt system that transforms raw property document packages into structured, one-page legal risk briefs — designed for real estate agents who need fast, clear decisions before client consultations.

---

📌 What This Is

This repository contains a structured **AI prompt template** built for Senior Real Estate Legal Analysis. It is designed to be used with large language models (LLMs) like Claude or GPT-4 to automatically analyze property document packages and produce a **standardized Due Diligence Brief** in under 3 minutes of reading time.

It is **not** legal software. It is a **decision-support tool** for real estate professionals.

---

🎯 Use Case

| Who It's For | What It Does |
|---|---|
| Real estate agents | Surfaces risks before client consultations |
| Transaction coordinators | Flags missing documents and disclosures |
| Buyer/seller representatives | Produces a fast, consistent risk summary |
| Brokerages | Standardizes due diligence across agents |

---

🗂️ Document Package Compatibility

The prompt accepts **any combination** of the following document types:

- Title history and chain of ownership records
- Purchase/sale agreements and addenda
- Property inspection reports (structural, electrical, plumbing, roof)
- Zoning certificates, land use permits, and variance approvals
- Environmental assessments (Phase I / Phase II)
- HOA bylaws, CC&Rs, and meeting minutes
- Mortgage records, outstanding liens, and encumbrances
- Seller disclosure statements and property history forms

---

📋 Output Structure

The prompt generates a **1-page Due Diligence Brief** with exactly 6 sections:

```
1. PROPERTY OVERVIEW
2. LEGAL RISKS
3. STRUCTURAL ISSUES
4. ZONING & REGULATORY RESTRICTIONS
5. FINANCIAL CONSIDERATIONS
6. RECOMMENDATION
```

Every bullet point carries a severity label: `[HIGH]`, `[MED]`, or `[LOW]`.

The brief ends with exactly one of three unambiguous recommendations:

```
PROCEED | PROCEED WITH CONDITIONS | DO NOT PROCEED
```

---

⚙️ Prompt Architecture

### Role Injection
The prompt opens by assigning the model a specific expert persona — a Senior Real Estate Legal Analyst with 15+ years of experience. This grounds the output in legal/technical vocabulary appropriate to the domain.

### Strict Output Rules (Non-Negotiable)
The prompt enforces 10 hard rules that govern every output:

| Rule | Purpose |
|---|---|
| Never suppress a legal risk | Completeness guarantee |
| Every bullet must have `[HIGH/MED/LOW]` | Consistent risk triage |
| Missing info → "Not disclosed — verify before proceeding." | Explicit gap flagging |
| No speculation beyond document content | Accuracy constraint |
| Bullet points only — no prose | Scannable format |
| Max 2 lines per bullet | Density constraint |
| Unambiguous recommendation — no hedging | Actionability |
| Exact dollar amounts and dates from source | Precision requirement |
| Section headers must not be renamed or reordered | Output consistency |
| Max ~500–600 words total | Fits on one printed page |

### Severity Framework

```
[HIGH]  → Requires immediate resolution before transaction proceeds
[MED]   → Should be addressed; may affect negotiation or closing terms
[LOW]   → Minor; monitor but unlikely to block the deal
```

### Recommendation Logic

```
PROCEED
  └─ No blocking issues identified

PROCEED WITH CONDITIONS
  └─ Issues present but resolvable
  └─ Each condition listed as an explicit bullet

DO NOT PROCEED
  └─ One or more blocking issues that cannot be resolved pre-closing
  └─ Each blocking issue listed explicitly
```

---

🚀 How to Use

### Option 1 — Paste Into an LLM Interface
1. Copy the full prompt from [`prompt.md`](./prompt.md)
2. Paste it into Claude, ChatGPT, or your preferred LLM
3. Attach or paste your property document package
4. The model returns a structured Due Diligence Brief


⚠️ Disclaimer

This tool is for **informational and decision-support purposes only**. It does **not** constitute legal advice. Outputs should be reviewed by a licensed attorney before being relied upon in any transaction. The prompt author and contributors are not liable for decisions made based on AI-generated briefs.

See [`DISCLAIMER.md`](./DISCLAIMER.md) for full terms.

---

🤝 Contributing

Pull requests are welcome. If you'd like to extend the prompt for additional document types — such as 1031 exchange agreements, ground leases, or commercial CAM reconciliations — please open an issue first to discuss scope.

---

📄 License

MIT License — free to use, modify, and distribute with attribution.
