---
title: "CPropertySheet::GetTabControl"
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
ms.assetid: 53250f63-b3ad-4741-b86d-d09e4a6ab0b4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::GetTabControl
Retrieves a pointer to a tab control to do something specific to the tab control (that is, to use any of the APIs in [CTabCtrl](../vs140/CTabCtrl-Class.md)).  
  
## Syntax  
  
```  
  
CTabCtrl* GetTabControl( ) const;  
  
```  
  
## Return Value  
 A pointer to a tab control.  
  
## Remarks  
 For example, call this member function if you want to add bitmaps to each of the tabs during initialization.  
  
## Example  
 [!CODE [NVC_MFCDocView#136](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#136)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::CTabCtrl](../vs140/CTabCtrl--CTabCtrl.md)