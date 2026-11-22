# Privacy Policy & Data Protection Disclosure

**Extension Name:** PortalBridge - Commercial Carrier Form Autofill  
**Effective Date:** November 2026  
**Last Updated:** November 2026  

---

## 1. Single Purpose Declaration
PortalBridge is an air-gapped commercial insurance productivity extension. Its sole purpose is to allow licensed insurance agents and customer service representatives (CSRs) to extract data from commercial insurance applications (such as ACORD forms) and populate that information into carrier rating portals and agency management systems directly within the user's active browser window.

---

## 2. Zero Remote Data Collection (Air-Gapped Guarantee)
* **No Remote Transmission:** PortalBridge **does not collect, transmit, host, sell, or share** any user data, commercial policyholder information, or file contents to any external server or third-party cloud service.
* **100% In-Browser Execution:** All PDF parsing, data normalization, and field matching are executed exclusively within the user's local browser memory (`ArrayBuffer` in client RAM).
* **Zero Telemetry:** The extension contains no analytics trackers, tracking cookies, advertising SDKs, or remote telemetry scripts.

---

## 3. Regulatory Compliance
PortalBridge is built specifically to meet the strict compliance requirements of the insurance industry:
* **Gramm-Leach-Bliley Act (GLBA):** Because policyholder Non-Public Personal Information (NPI) never leaves the agent's workstation, agencies remain fully compliant with GLBA privacy and safeguarding rules.
* **HIPAA & State Privacy Acts:** Any incidental health or commercial casualty information contained within loss runs or application forms remains isolated on the local endpoint.
* **SOC 2 Type II Alignment:** No customer data is stored, processed, or logged on developer infrastructure.

---

## 4. Permissions Disclosure & Usage
PortalBridge requests only the minimum permissions required under Manifest V3:
* **`sidePanel`:** Provides a persistent, side-by-side workspace to inspect parsed schedule records without covering the carrier portal.
* **`activeTab` & **`scripting`:** Injects framework-compatible input events into form controls on the active web tab upon user initiation.
* **`storage`:** Saves local UI theme preferences and offline cryptographic license activation keys locally on the device (`chrome.storage.local`).
* **`host_permissions: ["<all_urls>"]`:** Allows the extension to function across the hundreds of varied carrier rating domains, MGA portals, and agency management systems used daily by insurance professionals.

---

## 5. Contact & Inquiries
If you have questions regarding this privacy disclosure, please contact:
* **Repository:** [https://github.com/sjinsuretech/portalbridge-extension-](https://github.com/sjinsuretech/portalbridge-extension-)
* **Email:** sjinsuretech@gmail.com
