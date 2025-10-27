# Multi-Platform-Security-Auto-Refresher

# Privacy Policy for Multi-Platform Security Auto Refresher

**Last Updated:** October 27, 2025  
**Effective Date:** October 27, 2025  
**Version:** 1.0.0

---

## Table of Contents

- [Overview](#overview)
- [Information Collection and Use](#information-collection-and-use)
- [Data Transmission](#data-transmission)
- [Permissions Explained](#permissions-explained)
- [User-Created Content](#user-created-content)
- [Third-Party Services](#third-party-services)
- [Data Security](#data-security)
- [Data Retention](#data-retention)
- [Children's Privacy](#childrens-privacy)
- [International Users](#international-users)
- [Changes to This Privacy Policy](#changes-to-this-privacy-policy)
- [Compliance with Regulations](#compliance-with-regulations)
- [Open Source Transparency](#open-source-transparency)
- [Your Rights](#your-rights)
- [Contact Information](#contact-information)
- [Consent](#consent)
- [Specific Feature Privacy Notes](#specific-feature-privacy-notes)
- [Verification](#verification)
- [Legal Basis for Data Processing](#legal-basis-for-data-processing)
- [Summary](#summary)

---

## Overview

Multi-Platform Security Auto Refresher ("the Extension") is committed to protecting your privacy. This privacy policy explains how the Extension handles information when you use it.

**Key Point:** This Extension does not collect, transmit, or share any data. Everything operates locally on your device.

---

## Information Collection and Use

### We Do NOT Collect Any Data

**The Extension does not collect, transmit, or share any personal information or usage data.** All functionality operates entirely locally within your browser.

### What Data is Stored Locally

The Extension stores the following data **only on your local device** using Chrome's local storage API:

#### User Preferences
- Refresh interval settings (soft and hard refresh timings)
- Monitoring scope preferences (active tab or all tabs)
- Selected security platforms
- Notification settings (sounds, icons, timing)
- URL parser configurations (timezone, time range)

#### Operational Data
- Active monitoring session states
- Configuration profiles you create and name
- Task reminder schedules you set up
- Activity logs of refresh operations (last 200 entries only)
- Chronicle alerts you manually mark as "viewed"
- Custom notification sounds you upload (stored locally, max 50MB total)

### How Local Data is Used

All stored data serves only to:
- Remember your settings between browser sessions
- Maintain active monitoring sessions
- Execute scheduled refresh operations
- Track alerts you've reviewed
- Play your preferred notification sounds

**This data never leaves your device.** It is not transmitted to our servers, third-party services, or any external location.

---

## Data Transmission

### No External Network Requests

The Extension makes **zero external network requests**. Specifically:

| What We DON'T Do | Status |
|------------------|--------|
| Analytics or telemetry | ❌ Never |
| Tracking pixels or beacons | ❌ Never |
| Connection to remote servers | ❌ Never |
| Data uploaded to cloud services | ❌ Never |
| Third-party integrations | ❌ Never |
| Advertising networks | ❌ Never |
| User behavior tracking | ❌ Never |

### How the Extension Works

The Extension operates entirely within your browser:

1. **Content Scripts** inject into security platform pages you visit to detect and click refresh buttons
2. **Background Service Worker** manages timers and coordinates refresh operations
3. **Local Storage** saves your preferences on your device
4. **Chrome APIs** interact only with your browser (tabs, alarms, notifications)

All code execution happens locally. The Extension only interacts with the security platform pages you're actively using.

---

## Permissions Explained

The Extension requests several Chrome permissions. Here's why each is needed and how it protects your privacy:

### `activeTab`
- **Purpose:** Interact with the security platform page you're currently viewing
- **Privacy:** Only accesses the tab you're actively using, only when you trigger an action
- **Data Collected:** None
- **Data Transmitted:** None

### `alarms`
- **Purpose:** Schedule reliable refresh operations using Chrome's alarm system
- **Privacy:** Creates local timer events only
- **Data Collected:** None
- **Data Transmitted:** None

### `host (<all_urls>)`
- **Purpose:** Support multiple security platforms across different domains
- **Privacy:** Extension only activates on recognized security platform pages
- **Data Collected:** None
- **Data Transmitted:** None from any website
- **Note:** Required because security platforms use various domains:
  - `chronicle.security`
  - `falcon.crowdstrike.com`
  - `console.sentinelone.com`
  - `*.splunkcloud.com`
  - `*.elastic.co`
  - Custom enterprise deployments

### `notifications`
- **Purpose:** Display browser notifications for alerts and reminders
- **Privacy:** Notifications are generated locally only
- **Data Collected:** None
- **Data Transmitted:** None

### `offscreen`
- **Purpose:** Play notification sounds (required for Chrome Manifest V3)
- **Privacy:** Creates hidden audio-only page, no data collection
- **Data Collected:** None
- **Data Transmitted:** None

### `scripting`
- **Purpose:** Inject content scripts to click refresh buttons
- **Privacy:** Scripts only inject into security platform pages
- **Data Collected:** None
- **Data Transmitted:** None

### `storage`
- **Purpose:** Save your settings locally on your device
- **Privacy:** Uses `chrome.storage.local` (device-only, no sync)
- **Data Collected:** User preferences (stored locally)
- **Data Transmitted:** None

### `tabs`
- **Purpose:** Identify which security platform tabs are open
- **Privacy:** Only reads URLs/titles of open tabs to detect platforms
- **Data Collected:** None (tab information not stored permanently)
- **Data Transmitted:** None

---

## User-Created Content

### Custom JavaScript (Button Injection Feature)

The Extension includes a feature allowing advanced users to write custom JavaScript for injected buttons:

- This code is **written by you**, not fetched remotely
- It is **stored locally** in your browser's storage
- It **executes only** where you inject it
- **You have full control** to edit or delete it
- This is an **optional feature** for power users

**We do not access, collect, or transmit any custom code you create.**

### Custom Notification Sounds

You can upload custom audio files for notifications:

- Files are **stored locally** on your device only
- Maximum 5MB per file, 10 files total (50MB maximum)
- Files are **never transmitted** anywhere
- **You have full control** to delete uploaded files

---

## Third-Party Services

**The Extension does not integrate with any third-party services.** 

It does not:
- ❌ Connect to analytics platforms
- ❌ Use error tracking services
- ❌ Integrate with advertising networks
- ❌ Communicate with external APIs
- ❌ Share data with partners or affiliates

---

## Data Security

Since all data is stored locally on your device:

- **Your data security** depends on your device and browser security
- **Browser protection:** Chrome's security features protect your local storage
- **Extension removal:** Uninstalling the Extension deletes all stored data
- **Data clearing:** You can manually clear Extension data through Chrome settings

The Extension uses Chrome's secure storage APIs and follows Chrome Web Store security policies.

---

## Data Retention

### Automatic Retention Limits

| Data Type | Retention Policy |
|-----------|------------------|
| Activity Logs | Last 200 operations only |
| Monitoring Sessions | Cleared when monitoring stops or tabs close |
| User Settings | Retained until you delete or uninstall |
| Custom Sounds | Retained until you delete or uninstall |
| Alert "Viewed" Status | Retained until you delete or uninstall |

### How to Delete Your Data

You can delete Extension data at any time:

1. **Uninstall the Extension:** Removes all stored data permanently
2. **Clear through Chrome:** 
   - Settings → Privacy and security → Site Settings
   - Navigate to `chrome-extension://[extension-id]`
   - Clear storage
3. **Use Extension features:** Some tabs have "Clear" or "Delete" options for specific data

---

## Children's Privacy

The Extension is designed for security professionals and is not directed at children under 13. We do not knowingly collect information from children. The Extension's functionality (security platform monitoring) is intended for enterprise and professional use.

---

## International Users

The Extension operates entirely locally within your browser, regardless of your location. No data is transmitted internationally because **no data is transmitted at all**.

---

## Changes to This Privacy Policy

We may update this privacy policy to reflect:
- Changes in Chrome extension requirements
- New features added to the Extension
- Clarifications based on user questions

**Material changes** will be communicated through:
- Extension update notes in the Chrome Web Store
- Notification within the Extension (if applicable)

The "Last Updated" date at the top will reflect when changes were made.

---

## Compliance with Regulations

### GDPR (European Union)

The Extension complies with GDPR because:
- ✅ No personal data is collected or processed
- ✅ No data is transmitted to data controllers or processors
- ✅ All data remains on the user's device
- ✅ Users have full control to delete data

### CCPA (California)

The Extension complies with CCPA because:
- ✅ No personal information is collected or sold
- ✅ No data is shared with third parties
- ✅ Users have complete control over local data

### Other Regulations

Since the Extension does not collect, transmit, or process user data, it inherently complies with most data protection regulations worldwide.

---

## Open Source Transparency

The Extension's code is **not obfuscated** and can be inspected:

1. Download the Extension package from Chrome Web Store
2. Extract the files to review all source code
3. Verify no external network requests exist
4. Confirm all operations are local

**We encourage security-conscious users to review the code.**

---

## Your Rights

Since we don't collect your data, traditional data rights (access, deletion, portability) don't apply in the usual sense. However:

| Right | How to Exercise |
|-------|----------------|
| **Right to Control** | You control all local data through the Extension interface |
| **Right to Delete** | Uninstall the Extension to delete all data |
| **Right to Export** | Access Chrome's local storage via developer tools |
| **Right to Transparency** | Review this policy and the source code |

---

## Contact Information

If you have questions about this privacy policy or the Extension's data practices:

- **Extension Name:** Multi-Platform Security Auto Refresher
- **Developer:** [Your Name/Company Name]
- **Contact Email:** [Your Email Address]
- **Support:** [Support URL or Chrome Web Store support tab]
- **GitHub:** [Repository URL if applicable]

### Response Time

We aim to respond to privacy inquiries within **5 business days**.

---

## Consent

By installing and using the Extension, you acknowledge that:

- ✅ You have read and understood this privacy policy
- ✅ You understand that no data is collected or transmitted
- ✅ You understand that all data is stored locally on your device
- ✅ You can uninstall the Extension at any time to remove all data

---

## Specific Feature Privacy Notes

### Alert Monitoring
- ✅ Alert data is read from the security platform page DOM
- ✅ No alert data is stored permanently (only "viewed" status is saved locally)
- ✅ No alert data is transmitted anywhere

### URL Time Parser
- ✅ URL modifications happen locally in your browser
- ✅ No URLs are sent to external services
- ✅ Modified URLs remain in your browser history only

### Task Reminders
- ✅ Reminder schedules are stored locally only
- ✅ URLs you enter are stored locally only
- ✅ No reminder data is transmitted anywhere

### Button Injection
- ✅ Custom buttons are created from your local configuration
- ✅ Injected HTML/JavaScript runs only in your browser
- ✅ No injection data is transmitted anywhere

### Activity Logs
- ✅ Logs are stored locally only
- ✅ Last 200 operations only (automatic cleanup)
- ✅ No logs are transmitted anywhere

### Notification System
- ✅ Notifications are generated locally
- ✅ Custom sounds are stored locally only
- ✅ No notification data is transmitted anywhere

---

## Verification

**You can verify these privacy claims by:**

1. ✅ Using browser developer tools to monitor network activity (you'll see zero requests from the Extension)
2. ✅ Reviewing the Extension's source code (unobfuscated)
3. ✅ Checking Chrome's extension permissions page
4. ✅ Reviewing this privacy policy against the actual Extension behavior

---

## Legal Basis for Data Processing (GDPR)

Since no personal data is collected or processed, no legal basis for data processing is required under GDPR Article 6. The Extension operates purely as a local browser tool.

---

## Summary

### In Plain English:

| Privacy Aspect | Status |
|----------------|--------|
| Your data stays on your device | ✅ Yes |
| We don't collect anything | ✅ Confirmed |
| We don't transmit anything | ✅ Confirmed |
| We don't track you | ✅ Confirmed |
| You have full control | ✅ Yes |
| Uninstall = all data deleted | ✅ Yes |
| Source code is reviewable | ✅ Yes |

---

**This Extension is designed with privacy as a core principle. We believe security professionals deserve tools that respect their privacy while helping them do their jobs effectively.**

---

## Document Information

- **Document Version:** 1.0.0
- **Extension Version:** 1.0.0
- **Format:** Markdown (GitHub-compatible)

---

*For the most current version of this privacy policy, please visit Chrome Web Store listing.*

---

**© 2025 [CRB-CyberSec-Dev]. All rights reserved.**
