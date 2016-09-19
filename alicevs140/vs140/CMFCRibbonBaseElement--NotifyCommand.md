---
title: "CMFCRibbonBaseElement::NotifyCommand"
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
ms.assetid: 8af43ba1-6e82-45bf-bd1f-377538c96c85
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::NotifyCommand
Sends a command notification to the parent window of the ribbon element.  
  
## Syntax  
  
```  
BOOL NotifyCommand(  
   BOOL bWithDelay = FALSE  
);  
```  
  
#### Parameters  
 [in] `bWithDelay`  
 `TRUE` to add the command notification to the message queue of the parent window; `FALSE` to send the message immediately to the parent window.  
  
## Return Value  
 `TRUE` if the message was sent; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)