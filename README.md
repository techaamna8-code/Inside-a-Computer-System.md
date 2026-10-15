# Inside-a-Computer-System.md
Hand on Walkthroughs, and lab summaries covering TryHackMe's Pre-Security ans Foundation learning paths.
# TryHackMe: Inside a Computer System (Notes & Walkthrough)

Documentation and technical summary of the core hardware components and boot process from the **Inside a Computer System** room on TryHackMe.

---

## 📌 Room Overview
- **Platform:** TryHackMe
- **Category:** Pre Security > Computer Fundamentals
- **Objective:** Understand essential computing hardware building blocks, their functions, and the complete boot-up sequence from power-on to OS execution.

---

## ⚙️ Core Hardware Components (Human Body Analogy)

| Component | Analogy | Primary Function |
| :--- | :--- | :--- |
| **Motherboard** | Skeleton & Nerves | Main circuit board connecting all components and facilitating communication. |
| **CPU** | Brain | Executes instructions, handles calculations, and controls system operations. |
| **RAM** | Short-term Memory | Volatile high-speed memory storing active running programs and temporary data. |
| **HDD / SSD** | Long-term Memory | Non-volatile persistent storage for the Operating System, applications, and files. |
| **GPU** | Visual Cortex | Dedicated processing unit for rendering graphical calculations, UI, and video. |
| **PSU** | Heart & Lungs | Converts AC power to stable DC power and distributes it across all components. |

---

## 🔄 The Boot-Up Sequence

When the power button is pressed, the system initializes through a structured pipeline:

1. **Power-On:** Signal sent to the Power Supply Unit (PSU) to deliver electrical current to the motherboard and hardware.
2. **Firmware Initialization:** The system initializes low-level firmware (**UEFI / BIOS**) stored on non-volatile motherboard memory.
3. **POST (Power-On Self Test):** The firmware diagnostics scan critical hardware (RAM, CPU, storage) to ensure normal operating status before proceeding.
4. **Boot Device Selection:** Firmware evaluates the boot configuration order (configured drive, SSD/HDD, or external media) to locate the bootable partition.
5. **Bootloader Execution:** The system transfers control to the bootloader, which copies the Operating System kernel into RAM and launches system execution.

---

## 🛡️ Security Relevance
- Understanding hardware layout helps identify low-level attack vectors such as malicious firmware updates, rootkits, and bootloader manipulation (e.g., Secure Boot bypass).
- Knowledge of volatile memory (RAM) behavior is foundational for live memory forensics and artifact extraction.

---

*Status: Completed 100% on TryHackMe*
