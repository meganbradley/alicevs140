---
title: "CMenu::MeasureItem"
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
ms.assetid: a83565dc-7a9a-4adc-a6e0-67b7a6af2b06
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::MeasureItem
Called by the framework when a menu with the owner-draw style is created.  
  
## Syntax  
  
```  
  
      virtual void MeasureItem(  
   LPMEASUREITEMSTRUCT lpMeasureItemStruct   
);  
```  
  
#### Parameters  
 `lpMeasureItemStruct`  
 A pointer to a `MEASUREITEMSTRUCT` structure.  
  
## Remarks  
 By default, this member function does nothing. Override this member function and fill in the `MEASUREITEMSTRUCT` structure to inform Windows of the menu's dimensions.  
  
 See [CWnd::OnMeasureItem](../vs140/CWnd--OnMeasureItem.md) for a description of the `MEASUREITEMSTRUCT` structure.  
  
## Example  
 The following code is from the MFC [CTRLTEST](../vs140/Visual-C---Samples.md) sample:  
  
 [!CODE [NVC_MFCWindowing#31](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#31)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)