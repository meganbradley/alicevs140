---
title: "CMFCRibbonBaseElement::PostMenuCommand"
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
ms.assetid: 18cc763c-a373-4c8b-9acd-cdf46524af09
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::PostMenuCommand
Closes the pop-up menu for the ribbon element and sends a close message to the parent menu.  
  
## Syntax  
  
```  
void PostMenuCommand(  
   UINT uiCmdId  
);  
```  
  
#### Parameters  
 [in] `uiCmdId`  
 The parameter is not used.  
  
## Remarks  
 The close message is only sent if the ribbon element is located on a pop-up menu.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)