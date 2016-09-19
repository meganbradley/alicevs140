---
title: "CMFCRibbonCustomizeDialog::CMFCRibbonCustomizeDialog"
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
ms.assetid: 1308a9ed-d13f-4ee9-9e19-5199322aeb35
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCustomizeDialog::CMFCRibbonCustomizeDialog
Constructs a `CMFCRibbonCustomizeDialog` object.  
  
## Syntax  
  
```  
CMFCRibbonCustomizeDialog(  
   CWnd* pWndParent,  
   CMFCRibbonBar* pRibbon  
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 A pointer to the parent window (usually the main frame).  
  
 [in] `pRibbon`  
 A pointer to the `CMFCRibbonBar` that is to be customized.  
  
## Example  
 The following example demonstrates how to construct a `CMFCRibbonCustomizeDialog` object.  
  
 [!CODE [NVC_MFC_RibbonApp#18](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#18)]  
  
## Remarks  
 The constructor instantiates a [CMFCRibbonCustomizePropertyPage Class](../vs140/CMFCRibbonCustomizePropertyPage-Class.md) object and adds it to the collection of property sheet pages.  
  
## Requirements  
 **Header:** afxribboncustomizedialog.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonCustomizeDialog Class](../vs140/CMFCRibbonCustomizeDialog-Class.md)