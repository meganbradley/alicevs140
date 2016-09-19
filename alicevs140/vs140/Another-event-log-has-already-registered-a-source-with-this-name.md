---
title: "Another event log has already registered a source with this name"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e6f5cd95-bb3f-4845-84fb-ae623a9bd44e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Another event log has already registered a source with this name
An attempt was made to write an entry to an event log where the specified source is registered with another event log.  
  
 You must set the <xref:System.Diagnostics.EventLog.Source?qualifyHint=False> property of your <xref:System.Diagnostics.EventLog?qualifyHint=False> component instance before your component writes an entry to a log. When this happens, the system checks that the source you specified is registered with the event log to which the component is writing, and calls <xref:System.Diagnostics.EventLog.CreateEventSource?qualifyHint=False> if needed.  
  
### To correct this error  
  
1.  Remove the association of the source with the first log using the <xref:System.Diagnostics.EventLog.DeleteEventSource?qualifyHint=False> or the <xref:System.Diagnostics.EventLog.DeleteEventSource?qualifyHint=False> method.  
  
2.  Register the source with the new log.  
  
## See Also  
 [My.Application.Log Object](../Topic/My.Application.Log%20Object.md)   
 [How to: Remove an Event Source](assetId:///bc66c900-4b8a-426a-b8e2-17031a20167e)   
 [How to: Add Your Application as a Source of Event Log Entries](assetId:///948ff920-a739-4e66-a191-ee951512d42c)