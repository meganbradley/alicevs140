---
title: "CMFCReBar::GetReBarCtrl"
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
ms.assetid: 2093e44c-ac4c-47a5-800a-5e487d430b1d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCReBar::GetReBarCtrl
Provides direct access to `CReBarCtrl` the underlying common control for `CMFCReBar` objects.  
  
## Syntax  
  
```  
CReBarCtrl& GetReBarCtrl() const;  
```  
  
## Return Value  
 A reference to the underlying `CReBarCtrl` object.  
  
## Remarks  
 Call this method to take advantage of the Windows rebar common control functionality when customizing your rebar.  
  
## Requirements  
 **Header:** afxRebar.h  
  
## See Also  
 [CMFCReBar Class](../vs140/CMFCReBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)