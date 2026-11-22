# PortalBridge — Commercial Carrier Form Autofill

**Deterministic, Air-Gapped ACORD Form Autofill for Commercial Insurance Rating Portals & Agency Management Systems.**

---

## Overview

**PortalBridge** is a purpose-built Chrome browser extension engineered specifically for independent insurance agencies, retail brokerages, and commercial lines customer service representatives (CSRs).

Instead of re-typing client submission details across 4 to 6 different carrier rating portals, PortalBridge extracts commercial data directly from your agency's ACORD PDF applications and Statements of Values (SOVs), auto-populating carrier web forms with **100% deterministic precision**.

---

## Key Features

* **Instant ACORD & SOV Intake:** Drag-and-drop ACORD forms (125, 126, 140, 127) or Excel SOVs into the side panel for instant parsing in under 5 milliseconds.
* **100% Air-Gapped Local Processing:** Client documents and sensitive policyholder information are processed exclusively in client browser memory. **Zero data is transmitted to external cloud servers or public LLMs.**
* **Universal Carrier Compatibility:** Works across modern Single Page Applications (React, Angular, Vue) and legacy carrier portals (ASP.NET WebForms), automatically triggering underlying reactive framework bindings.
* **Multi-Pass Waterfall Automation:** Handles cascading carrier forms where conditional fields (such as LLC entity specifics, ISO construction types, or secondary locations) only render dynamically after initial trigger fields are entered.
* **Hard No-Submit Guardrail:** PortalBridge intentionally populates and formats the application but **never** submits, binds, or issues policies. The licensed agent or CSR retains full review authority before binding.
* **Click-to-Teach Field Mapping:** When carrier portals introduce custom underwriting questions, CSRs can map any field with a single click, saving the selector locally for future sessions.

---

## Supported Carrier Portals & AMS Platforms

PortalBridge is compatible out-of-the-box with leading commercial insurance rating platforms, including:

* **Travelers** (Commercial Express)
* **The Hartford** (E-Business Portal)
* **Liberty Mutual** (Commercial Lines Quoting)
* **Progressive Commercial**
* **CNA** (CNA Central)
* **Chubb** (Marketplace)
* **Agency Management Systems:** EZLynx, AgencyZoom, Applied Epic, AMS360, and HawkSoft.

---

## Security & Privacy Policy

> **Effective Date:** November 2026  
> **Privacy Contact:** support@portalbridge.internal

PortalBridge was architected from the ground up for commercial insurance compliance, adhering strictly to the **Gramm-Leach-Bliley Act (GLBA)**, state insurance department privacy regulations, and **SOC 2** standards.

### 1. Data Collection & Cloud Egress Disclosure
* **Zero Remote Data Collection:** PortalBridge does **not** collect, store, sell, or transmit any user data, policyholder Personally Identifiable Information (PII), or commercial documents to any remote server.
* **Client-Side In-Memory Execution:** Document ingestion and form autofill occur entirely inside the local user session. When the tab or browser is closed, all in-memory representations are discarded.
* **No Third-Party Analytics or Trackers:** PortalBridge contains no third-party tracking scripts, advertising SDKs, or background network telemetry.
* **Full Privacy Disclosure:** See our dedicated [PRIVACY.md](PRIVACY.md) policy for full compliance documentation.

### 2. Browser Permissions Justification
PortalBridge uses only the minimal set of Manifest V3 Chrome permissions necessary to deliver its core service:
* `sidePanel`: Displays the persistent side panel for reviewing commercial schedules and managing autofill without occluding carrier rating pages.
* `activeTab` & `scripting`: Dispatches native DOM input events to populate verified fields into the active carrier rating form upon explicit user command.
* `storage`: Persists local user preferences (such as light/dark mode and offline license authorization keys) directly on the user's machine via `chrome.storage.local`.
* `host_permissions: ["<all_urls>"]`: Enables autofill across the wide variety of carrier, MGA, and wholesaler quoting domains used by independent agencies.

---

## 30-Second Quick Start Guide

1. **Install PortalBridge** from the Chrome Web Store.
2. Click the **PortalBridge icon** in your Chrome toolbar to open the side panel.
3. Drag and drop any completed **ACORD 125** application PDF into the dropzone.
4. Navigate to your carrier rating portal (e.g., Travelers, Hartford, or Liberty Mutual).
5. Click **Auto-Fill Carrier Portal**.
6. Review the populated fields and proceed with underwriting as normal.

---

## Support & Inquiries

For technical support, feedback, or agency licensing inquiries, please open an issue in this repository or contact our support team.
