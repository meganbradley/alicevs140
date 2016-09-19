---
title: "CPropertySheet::EnableStackedTabs"
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
ms.assetid: 23938bcb-b2a1-4e5f-a025-6eeeda7182c4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::EnableStackedTabs
Indicates whether to stack rows of tabs in a property sheet.  
  
## Syntax  
  
```  
  
      void EnableStackedTabs(  
   BOOL bStacked   
);  
```  
  
#### Parameters  
 `bStacked`  
 Indicates whether stacked tabs are enabled in the property sheet. Disable stacked rows of tags by setting `bStacked` to **FALSE**.  
  
## Remarks  
 By default, if a property sheet has more tabs than will fit in a single row in the width of the property sheet, the tabs will stack in multiple rows. To use scrolling tabs instead of stacking tabs, call `EnableStackedTabs` with `bStacked` set to **FALSE** before calling [DoModal](../vs140/CPropertySheet--DoModal.md) or [Create](../vs140/CPropertySheet--Create.md).  
  
 You must call `EnableStackedTabs` when you create a modal or a modeless property sheet. To incorporate this style in a `CPropertySheet`-derived class, write a message handler for `WM_CREATE`. In the overridden version of [CWnd::OnCreate](../vs140/CWnd--OnCreate.md), call **EnableStackedTabs( FALSE )** before calling the base class implementation.  
  
## Example  
 [!CODE [NVC_MFCDocView#134](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#134)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)