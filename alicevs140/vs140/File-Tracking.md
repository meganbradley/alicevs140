---
title: "File Tracking"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e6c66ac0-3464-451f-9192-3b98dca21b4a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# File Tracking
File tracking logs calls to the Windows file system for a process and its child processes. By calling the functions listed below, programs control when to turn this logging on and off and specify the log file to use.  
  
## In This Section  
 [EndTrackingContext](../vs140/EndTrackingContext.md)  
 Stop tracking the current context.  
  
 [ResumeTracking](../vs140/ResumeTracking.md)  
 Resume tracking after a call to [SuspendTracking](../vs140/SuspendTracking.md).  
  
 [SetThreadCount](../vs140/SetThreadCount.md)  
 Set the number of threads to use for tracking.  
  
 [StartTrackingContext](../vs140/StartTrackingContext.md)  
 Begin a new tracking context.  
  
 [StartTrackingContextWithRoot](../vs140/StartTrackingContextWithRoot.md)  
 Begin a new tracking context with a specified root.  
  
 [StopTrackingAndCleanup](../vs140/StopTrackingAndCleanup.md)  
 End tracking and release resources used.  
  
 [SuspendTracking](../vs140/SuspendTracking.md)  
 Temporarily suspend tracking.  
  
 [WriteAllTLogs](../vs140/WriteAllTLogs.md)  
 Write out the tracking logs for all contexts.  
  
 [WriteContextTLogs](../vs140/WriteContextTLogs.md)  
 Write out the tracking log for the current context.