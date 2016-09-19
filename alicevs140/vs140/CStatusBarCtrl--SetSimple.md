---
title: "CStatusBarCtrl::SetSimple"
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
ms.assetid: 295ad863-118a-429f-8dd6-4639032c7330
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::SetSimple
Specifies whether a status bar control displays simple text or displays all control parts set by a previous call to [SetParts](../vs140/CStatusBarCtrl--SetParts.md).  
  
## Syntax  
  
```  
BOOL SetSimple(  
   BOOL bSimple = TRUE   
);  
```  
  
#### Parameters  
 [in] `bSimple`  
 Display-type flag. If this parameter is `TRUE`, the control displays simple text; if it is `FALSE`, it displays multiple parts.  
  
## Return Value  
 Always returns 0.  
  
## Remarks  
 If your application changes the status bar control from non-simple to simple, or vice versa, the system immediately redraws the control.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::SetParts](../vs140/CStatusBarCtrl--SetParts.md)