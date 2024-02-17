---
title: "Nexus Virus Check"
weight:
type: docs
description: >
  About the automatic virus checks on the Nexus.
---

All files that are uploaded to the Nexus will automatically be checked for viruses by [VirusTotal](https://www.virustotal.com/gui/home/upload).

You can view the report by clicking the **checkmark** in front of the file name.

![Nexus green](/Pictures/skyforge/knowledge-base/nexus-virus-check-green.png)

Files that exceed 250MB in size are manually verified. Occasionally, VirusTotal will detect *false positives* which usually happens with tools (see Mod Organizer 2) in which case the file is also manually verified.

## Mod Organizer 2

Mod Organizer 2 has been known to set off Antivirus software, usually due to the way that the UVFS is implemented. At times, it may still be flagged by one of the AVs used by VirusTotal in which case it will be manually verified by the Nexus that it is safe to use.

![MO2 Virus Total](/Pictures/skyforge/knowledge-base/mo2-virus-total.png)