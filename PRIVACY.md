# Privacy Policy & Data Protection Disclosure

**Extension Name:** PortalBridge - Commercial Carrier Form Autofill  
**Effective Date:** November 2026  
**Last Updated:** November 27, 2026  

---

## 1. Single Purpose Declaration
PortalBridge is a commercial insurance productivity extension. Its sole purpose is to allow licensed insurance agents and customer service representatives (CSRs) to parse commercial insurance applications (ACORD PDFs, Excel/CSV schedules, Loss Runs, and pasted renewal notes) locally in browser memory and populate those verified fields into commercial carrier rating portals and agency management systems within the user's active browser window.

---

## 2. Zero Policyholder Data Egress (Zero-PII Architecture)
* **Client Documents Stay in Browser RAM:** All PDF reading, binary stream decompression, Excel/CSV parsing, email/note parsing, E&O audits, and policyholder value population execute exclusively inside local browser memory (`ArrayBuffer` in client RAM). **Zero PDF files, insured names, FEINs, VINs, addresses, payrolls, revenues, or loss histories are transmitted to or stored on any external server.**
* **Zero Personal Account Data:** PortalBridge does **not** require email signup, personal profiles, passwords, IP logging, or geolocation tracking.
* **Stateless Mapping & Anonymous Seat Licensing:** When activating a license or mapping carrier forms, PortalBridge communicates with its encrypted Supabase Edge Functions strictly to:
  1. Verify cryptographic Ed25519 license keys against server UTC time and an anonymous random browser `device_id` UUID (`pb_licenses` / `pb_license_devices`).
  2. Fetch static ACORD extraction rules and map **empty carrier portal HTML form labels/attributes** (never field values or policyholder data) statelessly in server RAM.
* **Opt-In Public Registry Lookup:** Only when explicitly clicked by the user, PortalBridge queries public USDOT/MC carrier safety snapshots from the FMCSA registry (`safer.fmcsa.dot.gov`) using solely the public USDOT/MC number.
* **Zero Telemetry or Third-Party Cloud AI Sharing:** PortalBridge contains no analytics trackers, tracking cookies, advertising SDKs, or cloud LLM uploads.

---

## 3. Regulatory Compliance
PortalBridge is engineered specifically to align with insurance industry privacy standards:
* **Gramm-Leach-Bliley Act (GLBA):** Because policyholder Non-Public Personal Information (NPI) remains isolated in the agent's local browser session, agencies retain full data custody.
* **HIPAA & State Privacy Acts:** Any sensitive commercial or casualty details inside loss runs or application forms remain strictly on the local endpoint and are purged immediately via "Wipe Session RAM" or tab close.
* **SOC 2 Alignment:** Zero customer documents or policyholder records are stored or logged on developer infrastructure.

---

## 4. Permissions Disclosure & Usage
PortalBridge requests only the minimum permissions required under Manifest V3:
* **`sidePanel`:** Provides a persistent, side-by-side workspace to review extracted schedules without covering the carrier portal.
* **`activeTab` & `scripting`:** Injects framework-compatible DOM input events into form controls and embedded rating iframes on the active web tab strictly upon user initiation.
* **`storage`:** Stores UI preferences, an anonymous random `device_id`, local license session state (`chrome.storage.local`), and non-PII Click-to-Teach structural DOM selector rules (`IndexedDB`). Zero policyholder values are persisted.
* **`host_permissions: ["<all_urls>"]`:** Allows autofill across the hundreds of independent carrier rating domains, MGA portals, and agency management systems used daily by commercial insurance professionals (plus opt-in public FMCSA USDOT lookups).

---

## 5. Contact & Inquiries
If you have questions regarding this privacy disclosure, please contact:
* **Repository:** [https://github.com/sjinsuretech/portalbridge-extension-](https://github.com/sjinsuretech/portalbridge-extension-)
* **Email:** sjinsuretech@gmail.com
