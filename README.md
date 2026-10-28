Mobile Pentestration Testing and Ethical Hacking


EXP NO-1 — Browser-Based Android & ADB Essentials

Aim - To understand Android Debug Bridge (ADB) using WebADB and perform basic Android device enumeration, shell access, package management, activity management, and file-system navigation.

Description - This experiment demonstrates basic Android device interaction through a browser-based ADB interface. The practical includes connecting an authorized Android device, identifying the device using ADB, accessing the Android shell, inspecting installed packages, launching the Settings activity, and navigating the Android file system.


Exp No. 2 — Android Studio Installation and SDK Configuration

Aim - To install Android Studio and verify the Android SDK and required SDK tools for Android application development.

Tools -
Platform - Windows,
IDE	- Android Studio,
Android SDK	- Installed,
SDK Platform	- Android 17 (API 37),
Android Emulator	- Installed

Procedure -
1.	Installed Android Studio with the required Android SDK and emulator components.
2.	Opened Android SDK Manager and verified the installed SDK platform.
3.	Verified the required SDK tools including Build-Tools, Platform-Tools, Emulator, Command-line Tools, and Emulator Hypervisor Driver.
4.	Confirmed that the required SDK components were successfully installed and available.


Exp No. 3 – Android Architecture, Boot Process & Partition Layout

Aim - To examine the Android system architecture, boot-related information, mounted filesystems, and available block-device mappings of an Android emulator using ADB shell commands.

Procedure -
1.	Installed and configured Android Studio with the required Android SDK and emulator components. 
2.	Created and started a Pixel 9 Android Virtual Device. 
3.	Verified that the emulator was detected and connected through ADB. 
4.	Accessed the Android shell of the running emulator. 
5.	Examined the Android version, SDK/API level, and CPU architecture. 
6.	Inspected the Linux kernel information of the Android emulator. 
7.	Checked boot-related properties, including slot and verified-boot information. 
8.	Examined the mounted filesystems and storage usage of the emulator. 
9.	Inspected the available block-device mappings and their symbolic links. 
10.	Navigated through the /system, /vendor, and /product directories to examine the Android system file structure. 
11.	Recorded the observed system architecture, storage, filesystem, and partition-related information for analysis.

Commands Used -

adb devices

adb shell

getprop ro.build.version.release

getprop ro.build.version.sdk

getprop ro.product.cpu.abi

uname -a

getprop ro.boot.slot_suffix

getprop ro.boot.verifiedbootstate

cat /proc/cmdline

df -h

cat /proc/mounts

cat /proc/partitions

ls -l /dev/block/by-name

ls /system

ls /vendor

ls /product

exit


EXP NO-4 — APK Dissection Using Apktool and Android Emulator

Aim - To learn the basic workflow of APK analysis using Apktool and an Android Emulator by decoding an APK, inspecting its manifest and SMALI files, making a harmless UI modification, rebuilding, signing, and installing the APK.

Tools Used - Android Studio, Java JDK, Apktool, Android SDK Platform-Tools, Android SDK Build-Tools, Android Emulator, authorized training APK.

Procedure -
1. Created and started an Android Virtual Device.
2. Verified the emulator connection using ADB.
3. Installed the authorized training APK.
4. Decoded the APK using Apktool.
5. Inspected AndroidManifest.xml, permissions, exported components, and SMALI files.
6. Modified a harmless visible application label.
7. Rebuilt and signed the modified APK.
8. Installed the modified APK and verified the result.

Result - The APK analysis workflow was documented, including decoding, inspecting, modifying, rebuilding, signing, and installing the training application.


EXP NO-5 — JADX Decompilation and Hardcoded Secret Discovery

Aim - To analyze the authorized InsecureBankv2 application using JADX and identify hardcoded credentials, insecure URLs, debug flags, and logging-related security vulnerabilities.

Tools Used - JADX, Android Studio, Android Emulator, ADB, authorized InsecureBankv2 training APK.

Procedure -
1. Opened the authorized training APK in JADX.
2. Examined the decompiled application code and resources.
3. Searched for hardcoded credentials, secrets, insecure URLs, debug flags, and logging statements.
4. Reviewed the relevant code paths and application configuration.
5. Recorded observations and evidence for potential security issues.
6. Documented the security impact and recommended remediation.

Result - The static analysis workflow for identifying potential hardcoded secrets and other security weaknesses was documented.


EXP NO-6 — MobSF Static and Dynamic Analysis

Aim - To perform static and dynamic security analysis of the DIVA APK using Mobile Security Framework (MobSF) and an Android Emulator, and interpret findings such as CVSS scores, permissions, trackers, and runtime behavior.

Tools Used - MobSF, Android Studio, Android Emulator, DIVA APK, ADB.

Procedure -
1. Started the Android Emulator and verified connectivity using ADB.
2. Started MobSF and opened its web interface.
3. Uploaded the DIVA APK and waited for the static scan to complete.
4. Reviewed application information, permissions, security scores, CVSS findings, trackers, and manifest analysis.
5. Opened the Dynamic Analysis section and selected the running emulator.
6. Launched DIVA and interacted with its demonstration screens.
7. Examined runtime logs, API monitoring, and network traffic.
8. Recorded the observed security findings and analysis results.

Result - Static and dynamic analysis of the DIVA APK was documented, including relevant permissions, security findings, and runtime behavior.


EXP NO-7 — Burp Suite Proxy and SSL Pinning Bypass with Frida

Aim - To configure Burp Suite Community Edition as a proxy for an Android Emulator, inspect HTTPS traffic from an authorized test application, and demonstrate SSL-pinning bypass using Frida and Objection.

Tools Used - Burp Suite Community Edition, Frida, Objection, Android Studio Emulator, authorized training APK, ADB.

Procedure -
1. Configured a Burp Suite proxy listener on the host machine.
2. Configured the Android Emulator to use the Burp proxy.
3. Installed the Burp CA certificate in the test emulator.
4. Launched the authorized test application and checked its requests in Burp HTTP history.
5. Observed whether SSL pinning prevented HTTPS interception.
6. Started Frida Server on the test emulator.
7. Connected Objection/Frida to the authorized test application.
8. Performed the authorized SSL-pinning bypass demonstration.
9. Repeated the application request and checked the traffic in Burp.
10. Recorded the observations and restored the emulator's normal network configuration.

Result - The proxy configuration and SSL-pinning testing workflow was documented for an authorized mobile application.


EXP NO-8 — Frida Dynamic Instrumentation

Aim - To understand Frida Dynamic Instrumentation by writing JavaScript hooks to intercept function calls, observe application behavior at runtime, and monitor decryption and cryptographic API operations in an authorized test application.

Tools Used - Frida, Frida Server, Android Studio Emulator, authorized training APK, JADX, ADB.

Procedure -
1. Started the Android Emulator and verified the ADB connection.
2. Started Frida Server on the test emulator.
3. Opened the authorized training APK in JADX and identified relevant application methods.
4. Prepared a JavaScript hook for observing a selected application function.
5. Attached Frida to the running test application and observed function calls.
6. Examined a suitable decryption method and cryptographic API call in the authorized lab.
7. Captured the application screen and relevant console output as evidence.
8. Detached Frida and closed the testing session.

Result - Dynamic instrumentation was used to observe selected application functions and cryptographic operations at runtime.


EXP NO-9 — InsecureBankv2 Full Vulnerability Assessment

Aim - To assess the InsecureBankv2 training application for insecure login and session handling, local data exposure, weak cryptography indicators, and unsafe intent/component behavior.

Tools Used - InsecureBankv2 training APK, JADX, ADB, Burp Suite Community, Android Studio Emulator, Drozer where approved and compatible.

Procedure -
1. Started the Android Emulator and verified connectivity using ADB.
2. Examined the APK manifest using JADX to identify permissions, exported components, and deep links.
3. Searched the decompiled code for storage APIs, passwords, tokens, cryptographic functions, HTTP URLs, and intents.
4. Launched the training application using dummy test credentials.
5. Inspected authorized application traffic through the configured Burp proxy.
6. Reviewed transport security and session-management behavior.
7. Examined application storage using approved emulator/debugging access.
8. Reviewed exported components and potential intent-based data exposure.
9. Recorded reproducible evidence, security impact, and remediation for each confirmed finding.

Result - A structured vulnerability assessment was documented, including security observations, supporting evidence, and recommended remediation.


EXP NO-10 — ARM Disassembly with Ghidra and ROPgadget Basics

Aim - To identify the architecture and functions in an Android native library using Ghidra and understand how ROPgadget inventories instruction sequences.

Tools Used - Ghidra, ROPgadget, Android Studio Emulator, instructor-provided native .so sample.

Procedure -
1. Obtained an authorized native .so sample and created a working copy.
2. Created a non-shared project in Ghidra and imported the library.
3. Verified the file format and detected architecture.
4. Ran Ghidra Auto Analysis.
5. Examined the function list, disassembly, and decompiler output.
6. Recorded relevant function names and code observations.
7. Used ROPgadget, where available, to inventory instruction sequences for defensive analysis.
8. Captured screenshots of the function list and an annotated function view.

Result - The native library's architecture and functions were examined, and the disassembly workflow was documented.


EXP NO-11 — Kernel Module Compilation and Loading in Android Emulator

Aim - To understand the kernel-module build/load workflow and verify kernel compatibility in an Android Emulator.

Tools Used - Android Studio Emulator, ADB, GCC/Clang toolchain, Android kernel source/build configuration reference.

Procedure -
1. Started the emulator and verified connectivity using ADB.
2. Recorded the kernel version using adb shell uname -a.
3. Identified the device ABI using adb shell getprop ro.product.cpu.abi.
4. Compared the kernel information with the approved compatibility requirements.
5. Reviewed the sample kernel module source and its initialization and cleanup functions.
6. Checked whether the emulator supported loading the provided module.
7. Recorded the module-loading result and any security restrictions.
8. Checked the module list using adb shell lsmod and adb shell cat /proc/modules.
9. Documented the result without disabling or bypassing Android security controls.

Result - Kernel compatibility requirements and the module-loading restrictions of the Android Emulator were documented.


EXP NO-12 — AndroL4b CTF Challenges

Aim - To investigate intentionally vulnerable inter-app communication patterns, including intent snooping, insecure broadcasts, and deep-link hijacking, using the AndroL4b CTF environment.

Tools Used - AndroL4b approved CTF image/APK, Android Studio Emulator, JADX, ADB.

Procedure -
1. Set up the approved AndroL4b environment and verified the emulator connection.
2. Opened an assigned challenge and reviewed its description.
3. Inspected the application manifest using JADX.
4. Identified relevant exported activities, receivers, and intent filters.
5. Tested the challenge using the provided input within the isolated CTF environment.
6. Observed the resulting application behavior and checked relevant logs.
7. Captured screenshots showing the challenge and observed result.
8. Documented the vulnerable component, security impact, evidence, and recommended mitigation.
9. Reset the challenge environment before proceeding to another challenge.

Result - The assigned CTF challenge was investigated in an isolated emulator, and the observed behavior and security implications were documented.


EXP NO-13 — ASLR Demonstration and Address Randomization Observation

Aim - To observe address randomization across fresh process launches on the Android Emulator and explain how Address Space Layout Randomization (ASLR) reduces address predictability.

Tools Used - Android Studio Emulator, ADB shell, Python 3 for optional comparison and reporting.

Procedure -
1. Started the emulator and verified connectivity using ADB.
2. Checked the ASLR configuration, where accessible, using /proc/sys/kernel/randomize_va_space.
3. Launched a harmless sample application and identified its process ID.
4. Examined the process memory map and recorded a relevant library's base address.
5. Closed the application and relaunched it to obtain a new process ID.
6. Examined the memory map again and recorded the new address range.
7. Compared the recorded address ranges across the two runs.
8. Captured screenshots of the observations.
9. Documented the results without disabling ASLR or attempting to bypass it.

Result - Address randomization was examined across fresh process launches, and the observations were documented to explain ASLR's role in reducing address predictability.


EXP NO-14 — Full Mobile Penetration Testing Simulation on InsecureBankv2

Aim - To conduct a structured mobile penetration test on InsecureBankv2, covering reconnaissance, static analysis, dynamic analysis, controlled validation, and post-exploitation assessment, and document the findings.

Tools Used - JADX, MobSF, Burp Suite Community, Frida, Objection, ADB, Android Studio Emulator.

Procedure -
1. Defined the testing scope, target APK, emulator, test account, and permitted activities.
2. Performed reconnaissance by examining package information, SDK level, permissions, and exported components.
3. Conducted static analysis using JADX and MobSF.
4. Performed dynamic analysis using the emulator and inspected authorized application traffic through Burp Suite.
5. Used Frida/Objection for controlled validation of selected security weaknesses.
6. Examined the potential impact of confirmed findings, including sensitive data exposure and unauthorized component access.
7. Recorded reproducible evidence and assessed the impact and likelihood of each finding.
8. Recommended remediation for confirmed issues.
9. Restored the emulator to a clean state after testing.

Result - A structured mobile penetration-testing assessment was documented, covering reconnaissance, static and dynamic analysis, controlled validation, and remediation recommendations.


EXP NO-15 — Professional Penetration Testing Report Writing

Aim - To document the findings from Experiment 14 in a professional PTES/OWASP-style report, including an executive summary, technical findings, CVSS scoring, screenshots, and remediation recommendations.

Tools Used - LibreOffice Writer or MS Word, OWASP Mobile Application Security Testing Guide (MSTG), CVSS calculator.

Procedure -
1. Created the report structure with a title page, executive summary, scope, methodology, environment, findings, conclusion, and appendix.
2. Prepared the executive summary with the major risks and remediation priorities.
3. Documented the target application, testing environment, scope, and exclusions.
4. Described the methodology and tools used during Experiment 14.
5. Recorded each confirmed finding with its identifier, title, affected component, severity, reproduction steps, expected and actual results, impact, evidence, and remediation.
6. Assigned CVSS scores where required and documented the justification.
7. Redacted passwords, tokens, and identifying information from screenshots.
8. Cross-checked the findings against relevant OWASP MSTG categories.
9. Added a retest checklist for verifying the recommended fixes.
10. Proofread the report and exported it as a PDF.

Result - A professional penetration-testing report was prepared to document the findings from Experiment 14, their security impact, and recommended remediation.

