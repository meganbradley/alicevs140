---
title: "CPane::CopyState"
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
ms.assetid: 278786b9-0dd6-4dd4-aeca-6476c75f21f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::CopyState
Copies the state of a pane.  
  
## Syntax  
  
```  
virtual void CopyState(  
   CPane* pOrgBar  
);  
```  
  
#### Parameters  
 [in] `pOrgBar`  
 A pointer to a pane.  
  
## Remarks  
 This method copies the state of `pOrgBar` to the current pane.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)