<div align="center">
   
![openclaw](https://github.com/user-attachments/assets/c4a11654-02a9-412c-bd7a-16ee960eb919)

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-orange.svg)](LICENSE)

</div>

Enhance the security and privacy of your OpenClaw agents with these pre-configured, hardened SOUL.md templates. These files are designed to replace the default `soul.md` in existing OpenClaw configurations, providing strong safeguards against data leaks, prompt injection attacks, untrusted code execution, and accidental external actions.

<br>

## Overview

OpenClaw agents rely on a `soul.md` file to define their persona, behavior, and operating rules. The default templates prioritize helpfulness but leave agents vulnerable to several security risks, including exposure of sensitive data, unsafe external actions, and malicious third-party extensions.

These three templates offer progressively hardened configurations to help you:

* Maintain privacy and confidentiality of files, messages, and personal data.
* Enforce explicit verification for all external actions.
* Prevent untrusted code or skill execution.
* Mitigate prompt injection and social engineering attacks.
* Log all actions for full accountability and auditability.
* Operate safely within the principle of least privilege.

<br>

## Templates Included (listed in order of hardening)

1. **secure_soul.md** - Baseline Secure Posture
   Focused on general security best practices while maintaining internal assistance functionality. Protects sensitive data and enforces explicit consent for external actions.

<br>

2. **hardened_soul.md** - Enhanced Secure Posture
   Adds stricter runtime policies, including inline checks for external interactions, secrets handling, and prompt injection mitigation. Suitable for environments where external risks are significant.

<br>

3. **tamper_resistant_soul.md** - Maximum Secure Posture
   Full enforcement layer with templated runtime instructions. Every risky action triggers automatic verification, logging, and audit prompts. Ideal for semi-trusted or multi-user deployments requiring maximum safety.

<br>

## Installation (Step-by-Step)

Follow these instructions to update your `soul.md` file:

1. **Backup Your Current SOUL.md and SOUL_EVIL.md**

   * Open your OpenClaw workspace folder on your computer.
   * Locate the existing `soul.md` and `soul_evil.md` files.
   * If `soul_evil.md` does not exist, that is OK (disregard this file)
   * Right-click each file, select **Copy**, then **Paste** in the same folder.
   * Rename the copy to something like `soul_backup.md` or `soul_evil_backup.md` so you can restore it if needed.

2. **Download the Security Template**

   * Choose the soul.md template you want to use (above):

     * `secure_soul.md`
     * `hardened_soul.md`
     * `tamper_resistant_soul.md`
   * Click the **Raw** button to view the file content in plain text.

3. **Copy the File Content**

   * Select all the text in the raw view (**Ctrl+A / Cmd+A**).
   * Copy it to your clipboard (**Ctrl+C / Cmd+C**).

4. **Replace Your Existing SOUL.md and SOUL_EVIL.md**

   * Open the existing `soul.md` in your OpenClaw workspace with a text editor (Notepad, VS Code, Sublime, etc.).
   * Delete all existing content.
   * Paste the content from the clipboard (**Ctrl+V / Cmd+V**).
  
   * Open the existing `soul_evil.md` in your OpenClaw workspace with a text editor (Notepad, VS Code, Sublime, etc.).
   * Delete all existing content.
   * Paste the content from the clipboard (**Ctrl+V / Cmd+V**).

5. **Save the File**

   * Make sure the file name is exactly `soul.md` and soul_evil.md (case-sensitive on some systems).
   * Click **Save** for each.

6. **Restart OpenClaw**

   * Close and reopen your OpenClaw agent so it loads the new `soul.md`.

7. **Verify**

   * Ask your agent a simple question, like “What rules do you follow?”
   * Check that the agent responds according to the security template and does not attempt any external action without confirmation.

<br>

**Tips to Avoid Mistakes**

* Do not rename the file to anything other than `soul.md`. OpenClaw will ignore other names.
* If `soul_evil.md` does not exist that is OK. If it exists later, update it too.
* Always keep the backup file. If anything goes wrong, you can restore the original behavior.
* Use a text editor that preserves line breaks and formatting. Do not use rich-text editors like Word.
* These files are designed to be drop-in replacements, requiring no additional modifications to your agent to gain the security benefits.

<br>

## Usage Notes

* Always confirm external actions if prompted; these templates enforce verification by design.
* Do not remove or bypass sections related to prompt injection mitigation or secrets handling. Doing so will reduce the security guarantees.
* Logs and audit trails are internal only; review them periodically to ensure agent compliance.
* These templates are compatible with existing OpenClaw setups, but functionality that involves external communication or code execution may require explicit user consent.

<br>

## Contributing

Contributions are welcome for additional hardening strategies, best practices, or compatibility updates with newer OpenClaw releases. Please submit pull requests or issues with detailed descriptions and security reasoning.

<br>

## License

This repository is released under Apache 2.0

<br>
