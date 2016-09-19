---
title: "CMFCRibbonLinkCtrl::CMFCRibbonLinkCtrl"
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
ms.assetid: 7c77397e-956e-4470-a60e-295f1a775514
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonLinkCtrl::CMFCRibbonLinkCtrl
Constructs and initializes a [CMFCRibbonLinkCtrl](../vs140/CMFCRibbonLinkCtrl-Class.md) object.  
  
## Syntax  
  
```  
CMFCRibbonLinkCtrl(  
    UINT nID,  
    LPCTSTR lpszText,  
    LPCTSTR lpszLink   
);  
```  
  
#### Parameters  
 [in] `nID`  
 Specifies the command ID of the command that executes when the link control is clicked.  
  
 [in] `lpszText`  
 Specifies the label to display on the link control.  
  
 [in] `lpszLink`  
 Specifies the hyperlink associated with the link control.  
  
## Example  
 The following example demonstrates how to use the constructor of the `CMFCRibbonLinkCtrl` class. This code snippet is part of the [Ribbon Gadgets sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_RibbonGadgets#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonGadgets#1)]  
  
## Requirements  
 **Header:** afxRibbonLinkCtrl.h  
  
## See Also  
 [CMFCRibbonLinkCtrl Class](../vs140/CMFCRibbonLinkCtrl-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)