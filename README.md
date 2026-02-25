# Schedule 14D-9 Production Workflow

## Target's Solicitation / Recommendation Statement — LLM Capability Map v1.0

> **126 actionable steps** · **7 stages** · **5 validation gates** · **1 board deliberation freeze** · **9 SEC items**
> Covers the full production lifecycle from tender offer receipt through EDGAR filing within the 10-business-day deadline.

## LLM Capability Legend

| Color | Meaning | Node Style |
|-------|---------|------------|
| 🔴 Red | **LLM Cannot Do** — Human judgment, legal privilege, board decisions, sign-offs | Solid red fill |
| 🔴 Red (bold) | **Decision Diamond** — Human-only gate check | Dark red fill |
| 🔴 Red (dark) | **Milestone / Sign-Off** — Named accountability event | Deep red fill |
| 🟡 Yellow | **LLM Needs Human Oversight** — Can draft, human validates | Amber fill |
| 🟢 Green | **LLM Can Do Independently** — Research, formatting, compilation | Green fill |
| 🟢 Green (dark) | **Compile Step** — LLM assembles section from approved inputs | Dark green fill |

## Sign-Off Types

| Type | Meaning | Who |
|------|---------|-----|
| **ATTESTATION** | Factual data is accurate and verified | Management, Financial Advisor |
| **CERTIFICATION** | Document is production-ready, all items addressed, privilege-safe | Lead Counsel |
| **APPROVAL** | Board recommendation endorsed and authorized for filing | Board / Special Committee |
| **PREREQUISITE** | SEC disclosure and regulatory requirements fulfilled | SEC Counsel |

---

## Pre-Production: Engagement & Mobilization

> *Entirely 🔴 — board-level engagement decisions, privilege establishment, timeline calculation. The 10-business-day clock starts when the TO is filed.*

```mermaid
flowchart TD
  A(["Tender offer received / TO filed"]):::red --> B["Engage outside legal counsel"]:::red
  B --> C["Engage financial advisor"]:::red
  C --> D{"Conflicts requiring Special Committee?"}:::redD
  D -- Yes --> E["Form Special Committee & retain independent counsel"]:::red
  D -- No --> F
  E --> F["Establish data room & privilege protocols"]:::red
  F --> G["Calculate 10-business-day response deadline"]:::yel
  G --> H["Assign production roles & workstreams"]:::red
  H --> I["Establish document version control"]:::yel
  I --> J["Initial board briefing on TO terms & timeline"]:::red
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef redD fill:#f87171,stroke:#dc2626,color:#7f1d1d,font-weight:700
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
```

## 🚧 Gate 1: Factual Foundation Lock

> *Before any drafting begins, all transaction facts must be extracted, verified, and locked. Management attests to factual accuracy.*

```mermaid
flowchart TD
  A["Extract terms from TO / merger agreement"]:::yel --> B["Verify offer price, form of consideration, timing"]:::red
  B --> C["Confirm bidder identity & financing commitments"]:::red
  C --> D["Cross-check against bidder's public filings"]:::grn
  D --> E{"All transaction facts locked?"}:::redD
  E -- No --> A
  E -- Yes --> F["Management: ATTESTATION ✓"]:::redM
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef redD fill:#f87171,stroke:#dc2626,color:#7f1d1d,font-weight:700
  classDef redM fill:#dc2626,stroke:#b91c1c,color:#fff,font-weight:700
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
```

## Stage 1: Transaction Summary — Items 1–2

> *Mostly 🟢 — factual company information and transaction terms pulled from locked data. LLM compiles from verified inputs.*

```mermaid
flowchart TD
  A["Subject company information"]:::grn --> B["Identity & background of filing person"]:::grn
  B --> C["Transaction terms: price, structure, conditions"]:::yel
  C --> D["Financing structure & sources"]:::yel
  D --> E["Conditions to the offer"]:::yel
  E --> F["Compile Items 1–2"]:::grnC
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
  classDef grnC fill:#16a34a,stroke:#15803d,color:#fff,font-weight:700
```

## Stage 2: Background of the Transaction

> *The most sensitive section. Blow-by-blow narrative of how the deal unfolded. Heavy 🔴 — board minutes, director interviews, privilege review. LLM can draft narrative from records but every paragraph needs legal review.*

```mermaid
flowchart TD
  A["Collect board minutes & committee records"]:::red --> B["Interview directors & management participants"]:::red
  B --> C["Compile chronological contact log"]:::yel
  C --> D["Draft initial approach / first contact narrative"]:::yel
  D --> E["Draft negotiation phases & term evolution"]:::yel
  E --> F["Draft competing / topping bid history"]:::yel
  F --> G["Draft advisor engagement & mandate timeline"]:::yel
  G --> H["Draft board / committee meeting narrative"]:::yel
  H --> I["Privilege review of all cited communications"]:::red
  I --> J["Cross-reference against document retention log"]:::red
  J --> K["Compile Background section"]:::grnC
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grnC fill:#16a34a,stroke:#15803d,color:#fff,font-weight:700
```

## 🚧 Gate 2: Background Narrative Verification

> *Every factual claim in the background verified against board records. Privilege review ensures no inadvertent waiver. Lead Counsel attests.*

```mermaid
flowchart TD
  A["Every meeting / contact verified vs. board records"]:::red --> B["Privilege review complete — no waiver risk"]:::red
  B --> C["Timeline internally consistent"]:::grn
  C --> D["Competing bid disclosure complete & accurate"]:::red
  D --> E{"All verified & privilege-safe?"}:::redD
  E -- No --> A
  E -- Yes --> F["Lead Counsel: ATTESTATION ✓"]:::redM
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef redD fill:#f87171,stroke:#dc2626,color:#7f1d1d,font-weight:700
  classDef redM fill:#dc2626,stroke:#b91c1c,color:#fff,font-weight:700
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
```

## Stage 3: Financial Analysis & Projections

> *Valuation summary drafting is heavily 🟢 — LLM formats comp tables, precedent transactions, DCF summaries. Management projections (🔴) require board approval. Financial advisor must review final summary for accuracy.*

```mermaid
flowchart TD
  A["Receive financial advisor's preliminary analysis"]:::red --> B["Draft comparable companies analysis summary"]:::grn
  B --> C["Draft precedent transactions summary"]:::grn
  C --> D["Draft DCF analysis summary"]:::grn
  D --> E["Draft premiums paid analysis"]:::grn
  E --> F["Draft other methodologies (LBO, sum-of-parts)"]:::grn
  F --> G["Document assumptions & limitations for each method"]:::yel
  G --> H["Receive management projections (board-approved)"]:::red
  H --> I["Draft projection tables with key line items"]:::yel
  I --> J["Document projection methodology & key assumptions"]:::yel
  J --> K["Financial advisor reviews summary for accuracy"]:::red
  K --> L["Compile Financial Analysis section"]:::grnC
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
  classDef grnC fill:#16a34a,stroke:#15803d,color:#fff,font-weight:700
```

## 🚧 Gate 3: Fairness Opinion Lock

> *Fairness opinion letter received in final form. Summary in the 14D-9 must accurately reflect the full opinion. Financial advisor attests to accuracy.*

```mermaid
flowchart TD
  A["Final fairness opinion letter received"]:::red --> B["Summary accurately reflects full opinion"]:::red
  B --> C["Projections in 14D-9 match advisor's inputs"]:::yel
  C --> D["Assumptions & limitations properly disclosed"]:::red
  D --> E{"Advisor confirms summary accuracy?"}:::redD
  E -- No --> B
  E -- Yes --> F["Financial Advisor: ATTESTATION ✓"]:::redM
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef redD fill:#f87171,stroke:#dc2626,color:#7f1d1d,font-weight:700
  classDef redM fill:#dc2626,stroke:#b91c1c,color:#fff,font-weight:700
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
```

## ⚠ Board Deliberation — Required Before Recommendation

> *New in this workflow. The board must formally deliberate and vote before the recommendation and reasons sections can be drafted. All 7 nodes are 🔴 — this is a purely human governance event. No drafting of the recommendation may begin until this checkpoint clears.*

```mermaid
flowchart TD
  BD1["Present financial analysis to board / committee"]:::red --> BD2["Present strategic alternatives analysis"]:::red
  BD2 --> BD3["Legal counsel advises on fiduciary duties"]:::red
  BD3 --> BD4["Board deliberation (recorded in minutes)"]:::red
  BD4 --> BD5["Board / committee votes on recommendation"]:::red
  BD5 --> BD6{"Recommendation locked?"}:::redD
  BD6 -- No --> BD1
  BD6 -- Yes --> BD7["Board Chair / Committee Chair: APPROVAL ✓"]:::redM
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef redD fill:#f87171,stroke:#dc2626,color:#7f1d1d,font-weight:700
  classDef redM fill:#dc2626,stroke:#b91c1c,color:#fff,font-weight:700
```

## Stage 4: Recommendation & Reasons

> *Mostly 🟡 — LLM drafts from board deliberation records, but every sentence needs legal review for fiduciary compliance. Dissenting views (🔴) are board-only. Revlon/Unocal review is outside counsel's domain.*

```mermaid
flowchart TD
  A["Draft recommendation statement (accept / reject / no position)"]:::yel --> B["Document positive factors considered"]:::yel
  B --> C["Document negative factors & risks considered"]:::yel
  C --> D["Document neutral / uncertain factors"]:::yel
  D --> E["Draft balancing analysis & weighing of factors"]:::yel
  E --> F["Document process safeguards relied upon"]:::yel
  F --> G["Document dissenting views (if any)"]:::red
  G --> H["Legal review — Revlon / Unocal / fiduciary compliance"]:::red
  H --> I["Compile Recommendation & Reasons"]:::grnC
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grnC fill:#16a34a,stroke:#15803d,color:#fff,font-weight:700
```

## Stage 5: Conflicts, Interests & Governance

> *Mixed 🔴/🟡 — equity holdings and golden parachute math are LLM-computable from data. Change-of-control terms, employment arrangements, and director relationships with the bidder require human disclosure. Legal reviews completeness.*

```mermaid
flowchart TD
  A["Director & officer equity holdings"]:::yel --> B["Stock options, RSUs, equity award treatment"]:::yel
  B --> C["Change-of-control / severance provisions"]:::red
  C --> D["Golden parachute calculations (Item 402(t))"]:::yel
  D --> E["Ongoing employment / consulting arrangements with bidder"]:::red
  E --> F["Director relationships or arrangements with bidder"]:::red
  F --> G["Special Committee independence confirmation"]:::red
  G --> H["Quantify total payments per individual"]:::yel
  H --> I["Draft Item 3 — interests & conflicts table"]:::yel
  I --> J["Legal review — completeness of conflict disclosures"]:::red
  J --> K["Compile Conflicts & Interests section"]:::grnC
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grnC fill:#16a34a,stroke:#15803d,color:#fff,font-weight:700
```

## Stage 6: Legal, Regulatory & Shareholder Rights

> *Heavy 🔴 — regulatory filings, intent to tender, and SEC compliance are counsel-driven. Appraisal rights drafting (🟡) uses state-law boilerplate but needs jurisdiction-specific review. Safe harbor language is 🟢.*

```mermaid
flowchart TD
  A["Appraisal / dissent rights analysis"]:::yel --> B["Draft appraisal rights notice language"]:::yel
  B --> C["Identify regulatory approvals required (HSR, CFIUS, etc.)"]:::red
  C --> D["Status of regulatory filings & expected timeline"]:::red
  D --> E["Forward-looking statements safe harbor language"]:::grn
  E --> F["Information about the subject company"]:::grn
  F --> G["Intent to tender disclosures (directors & officers)"]:::red
  G --> H["SEC compliance review — Regulation 14D"]:::red
  H --> I["Compile Legal & Regulatory sections"]:::grnC
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
  classDef grnC fill:#16a34a,stroke:#15803d,color:#fff,font-weight:700
```

## 🚧 Gate 4: SEC Compliance Lock

> *Regulatory checkpoint. Every Schedule 14D-9 item addressed, Regulation 14D compliance confirmed, appraisal rights properly noticed. SEC Counsel provides governance prerequisite.*

```mermaid
flowchart TD
  A["Schedule 14D-9 item checklist — all items addressed"]:::grn --> B["Regulation 14D-101 compliance verified"]:::red
  B --> C["Appraisal rights properly noticed per state law"]:::red
  C --> D["Golden parachute calculations verified by counsel"]:::red
  D --> E{"All disclosure requirements met?"}:::redD
  E -- No --> A
  E -- Yes --> F["SEC Counsel: PREREQUISITE ✓"]:::redM
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef redD fill:#f87171,stroke:#dc2626,color:#7f1d1d,font-weight:700
  classDef redM fill:#dc2626,stroke:#b91c1c,color:#fff,font-weight:700
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
```

## Stage 7: Exhibits & Final Assembly

> *Mixed — exhibit attachment is 🔴 (legal instruments). Shareholder letter drafting is 🟡. Cross-referencing, compilation, and proofing are 🟢. EDGAR formatting is 🟡.*

```mermaid
flowchart TD
  A["Attach fairness opinion letter (Exhibit (a))"]:::red --> B["Attach or incorporate merger agreement"]:::red
  B --> C["Draft letter to shareholders"]:::yel
  C --> D["Prepare information statement (if required)"]:::yel
  D --> E["Compile exhibit index"]:::grn
  E --> F["Assemble full document"]:::grnC
  F --> G["Cross-reference verification"]:::grn
  G --> H["EDGAR formatting & filing codes"]:::yel
  H --> I["Final proofread"]:::grn
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
  classDef grnC fill:#16a34a,stroke:#15803d,color:#fff,font-weight:700
```

## 🚧 Gate 5: Final Review & Filing Authorization

> *12 QC checks followed by 4-tier sign-off chain. Board authorizes filing as final step before EDGAR submission. Sign-off order: attestations → certification → approval.*

```mermaid
flowchart TD
  Q1["All Schedule 14D-9 items addressed"]:::grn --> Q2["Financial figures consistent throughout"]:::grn
  Q2 --> Q3["Background narrative matches board minutes"]:::red
  Q3 --> Q4["Fairness opinion summary approved by advisor"]:::red
  Q4 --> Q5["Golden parachute calculations verified"]:::yel
  Q5 --> Q6["Appraisal rights properly noticed"]:::red
  Q6 --> Q7["Forward-looking statements disclaimered"]:::grn
  Q7 --> Q8["Privilege review — no inadvertent disclosure"]:::red
  Q8 --> Q9["Exhibit list complete & attached"]:::grn
  Q9 --> Q10["EDGAR formatting verified"]:::yel
  Q10 --> Q11["Filing within 10-business-day deadline confirmed"]:::red
  Q11 --> Q12["Board / committee authorizes filing"]:::red
  Q12 --> QP{"All checks pass?"}:::redD
  QP -- No --> Q1
  QP -- Yes --> S1x["Management: ATTESTATION ✓"]:::redM
  S1x --> S2x["Financial Advisor: ATTESTATION ✓"]:::redM
  S2x --> S3x["Lead Counsel: CERTIFICATION ✓"]:::redM
  S3x --> S4x["Board / Special Committee: APPROVAL ✓"]:::redM
  S4x --> DONE(["📄 FILED WITH SEC VIA EDGAR"]):::redM
  classDef red fill:#fecaca,stroke:#dc2626,color:#7f1d1d
  classDef redD fill:#f87171,stroke:#dc2626,color:#7f1d1d,font-weight:700
  classDef redM fill:#dc2626,stroke:#b91c1c,color:#fff,font-weight:700
  classDef yel fill:#fef3c7,stroke:#d97706,color:#78350f
  classDef grn fill:#dcfce7,stroke:#16a34a,color:#14532d
```

---

## Capability Summary

| Category | Approx. Steps | Examples |
|----------|:---:|---------|
| 🔴 **LLM Cannot Do** | ~66 | Board deliberations, privilege review, sign-offs, fairness opinion, management interviews, director conflicts, SEC compliance, regulatory filings, fiduciary review |
| 🟡 **LLM Needs Human Oversight** | ~34 | Background narrative drafting, projection tables, golden parachute calculations, recommendation factors, appraisal rights language, EDGAR formatting |
| 🟢 **LLM Can Do** | ~26 | Comparable company summaries, precedent transactions, DCF formatting, cross-reference checks, safe harbor language, item checklists, exhibit compilation, proofreading |

## Key Differences from IC Memo Workflow

| Dimension | IC Memo (184 steps) | Schedule 14D-9 (126 steps) |
|-----------|----|----|
| **Primary drafter** | Memo Owner (internal team) | Outside Legal Counsel |
| **Ultimate authority** | Deal Sponsor | Board of Directors / Special Committee |
| **Freeze checkpoint** | Decision-Rights Freeze (lock ask before valuation) | Board Deliberation (lock recommendation before drafting reasons) |
| **Time pressure** | Weeks to months | 10 business days from TO filing |
| **Regulatory overlay** | Firm governance only | SEC Regulation 14D, state appraisal law, fiduciary duty standards |
| **Privilege concern** | Confidentiality tiers | Attorney-client privilege — inadvertent waiver risk |
| **LLM-heavy areas** | Market research, comps, scenario modeling | Valuation summaries, financial tables, boilerplate legal language |
| **LLM-restricted areas** | Sign-offs, deal terms, personnel | Board decisions, privilege review, fiduciary analysis, conflict disclosures |
| **Red/Yellow/Green split** | 62 / 66 / 56 (34% / 36% / 30%) | 66 / 34 / 26 (52% / 27% / 21%) |

## Usage

1. **Clone** this repo and open the `.mermaid` file in any Mermaid-compatible viewer.
2. **README.md** renders natively on GitHub with embedded flowcharts.
3. **HTML presentation** opens in any browser — dark-themed, scroll-animated, sidebar navigation.

---

*Schedule 14D-9 Production Workflow v1.0 | LLM Capability Map | Confidential*
