---
title: "CMFCRibbonBar::SetApplicationButton"
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
ms.assetid: 8568e48a-a878-4c7a-89a4-b7ab795da7f0
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::SetApplicationButton
Assigns an application ribbon button to the ribbon bar.  
  
## Syntax  
  
```  
void SetApplicationButton(  
   CMFCRibbonApplicationButton* pButton,  
   CSize sizeButton   
);  
```  
  
#### Parameters  
 [in] `pButton`  
 A pointer to the application ribbon button.  
  
 [in] `sizeButton`  
 The size of the application ribbon button.  
  
## Remarks  
 The application ribbon button is a large rounded button located at the upper-left corner of Ribbon control.  
  
## Example  
 The following example demonstrates how to use the `SetApplicationButton` method in the `CMFCRibbonBar` class.  
  
 [!CODE [NVC_MFC_RibbonApp#3](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#3)]  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)