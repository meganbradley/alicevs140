---
title: "CHtmlEditCtrlBase::QueryStatus"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: cfc88c61-3661-411f-9011-f4f6679c03d7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::QueryStatus
Call this method to query the status of commands.  
  
## Syntax  
  
```  
  
      long QueryStatus(  
   long cmdID   
) const;  
```  
  
#### Parameters  
 `cmdID`  
 The command ID. Command identifiers are taken from the `CGID_MSHTML`command group. These commands are defined in Mshtmcid.h. You can also find the list online at [MSHTML Command Identifiers](http://go.microsoft.com/fwlink/?LinkId=149220).  
  
## Return Value  
 Returns an [OLECMDF](http://msdn.microsoft.com/library/windows/desktop/ms695237) indicating the status for `cmdID`, or 0 on failure.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [IOleCommandTarget::QueryStatus](http://msdn.microsoft.com/library/windows/desktop/ms688491)   
 [MSHTML Command Identifiers](http://go.microsoft.com/fwlink/?LinkId=149220)