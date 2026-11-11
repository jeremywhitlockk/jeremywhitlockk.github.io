---
title: "I Audited My Own iOS App. Here's What I Found"
date: 2026-11-29 10:00:00 -0500
categories: [iOS Security, Audits]
tags: [ios, owasp-masvs, mobsf, swift, appsec]
description: What a security review of an app I built myself turned up, and how I fixed each issue.
---

<!--
DRAFT. This lives in _drafts/, so it is NOT published.
To publish: fill it in, then move it to _posts/ and rename it to
YYYY-MM-DD-i-audited-my-own-ios-app.md (e.g. 2026-11-29-i-audited-my-own-ios-app.md).

Tips:
- Write it in your own voice; short paragraphs.
- NEVER paste a real API key or token. Rotate any key you find, and show it as sk_live_****.
- Screenshots go in assets/img/posts/ and are added with ![alt text](/assets/img/posts/file.png)
-->

## Why I did this

<!-- 2–3 sentences: you build iOS apps, wanted to see your own work from an attacker's view. What's the app? (one line, no sensitive details) -->

## How I tested it

<!-- Tools and approach. Example: -->
- Read the iOS chapters of the [OWASP MASTG](https://mas.owasp.org/MASTG/)
- Ran the .ipa through [MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF)
- Manually reviewed Info.plist, data storage, Keychain usage and logging
- Checked what the app writes to disk using the iOS Simulator's app container

## What I found

<!-- One subsection per finding. Lead with the most serious. -->

### 1. <!-- Finding title, e.g. "Auth token stored in UserDefaults" -->

- **Severity:** <!-- High / Medium / Low -->
- **MASVS:** <!-- e.g. MASVS-STORAGE-1 -->
- **What was wrong:** <!-- one or two sentences -->
- **Why it matters:** <!-- how an attacker could use it -->

```swift
// Before
```

```swift
// After
```

### 2. <!-- Next finding -->

## What MobSF missed (or over-reported)

<!-- Which findings were false positives? Did you find anything manually that the scanner didn't? This sets up the tool you're building. -->

## What I learned

<!-- 3–4 bullets: the mistakes you'll never make again. -->

## What's next

I'm turning these lessons into an open-source tool, [ios-security-auditor](https://github.com/jeremywhitlockk/ios-security-auditor), that catches these issues automatically and uses an LLM to filter out false positives. Follow along on GitHub.
