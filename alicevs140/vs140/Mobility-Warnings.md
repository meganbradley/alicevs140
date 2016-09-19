---
title: "Mobility Warnings"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9808054c-593b-4fc3-92cc-1fc45f41569c
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mobility Warnings
Mobility warnings support efficient power usage.  
  
## In This Section  
  
|Rule|Description|  
|----------|-----------------|  
|[CA 1600: Do not use idle process priority](../vs140/CA1600--Do-not-use-idle-process-priority.md)|Do not set process priority to Idle. Processes that have System.Diagnostics.ProcessPriorityClass.Idle will occupy the CPU when it would otherwise be idle, and will therefore block standby.|  
|[CA 1601: Do not use timers that prevent power state changes](../vs140/CA1601--Do-not-use-timers-that-prevent-power-state-changes.md)|Higher-frequency periodic activity will keep the CPU busy and interfere with power-saving idle timers that turn off the display and hard disks.|