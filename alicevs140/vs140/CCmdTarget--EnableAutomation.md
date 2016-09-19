---
title: "CCmdTarget::EnableAutomation"
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
ms.assetid: d71526d5-e481-4367-a937-b8c959cd43e3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::EnableAutomation
Call this function to enable OLE automation for an object.  
  
## Syntax  
  
```  
  
void EnableAutomation( );  
```  
  
## Remarks  
 This function is typically called from the constructor of your object and should only be called if a dispatch map has been declared for the class. For more information on automation see the articles [Automation Clients](../vs140/Automation-Clients.md) and [Automation Servers](../vs140/Automation-Servers.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DECLARE_DISPATCH_MAP](../vs140/DECLARE_DISPATCH_MAP.md)   
 [DECLARE_OLECREATE](../vs140/DECLARE_OLECREATE.md)