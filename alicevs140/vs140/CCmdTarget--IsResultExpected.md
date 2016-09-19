---
title: "CCmdTarget::IsResultExpected"
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
ms.assetid: f8999cbf-cbc3-447a-9674-e376ad28b0b3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::IsResultExpected
Use `IsResultExpected` to ascertain whether a client expects a return value from its call to an automation function.  
  
## Syntax  
  
```  
  
BOOL IsResultExpected( );  
```  
  
## Return Value  
 Nonzero if an automation function should return a value; otherwise 0.  
  
## Remarks  
 The OLE interface supplies information to MFC about whether the client is using or ignoring the result of a function call, and MFC in turn uses this information to determine the result of a call to `IsResultExpected`. If production of a return value is time- or resource-intensive, you can increase efficiency by calling this function before computing the return value.  
  
 This function returns 0 only once so that you will get valid return values from other automation functions if you call them from the automation function that the client has called.  
  
 `IsResultExpected` returns a nonzero value if called when an automation function call is not in progress.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::GetIDispatch](../vs140/CCmdTarget--GetIDispatch.md)   
 [CCmdTarget::EnableAutomation](../vs140/CCmdTarget--EnableAutomation.md)