---
title: "CMFCKeyMapDialog::CMFCKeyMapDialog"
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
ms.assetid: d12e7488-996e-4b43-9b41-e7c29e7617d9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCKeyMapDialog::CMFCKeyMapDialog
Constructs a `CMFCKeyMapDialog` object.  
  
## Syntax  
  
```  
CMFCKeyMapDialog(  
   CFrameWnd* pWndParentFrame,  
   BOOL bEnablePrint=FALSE   
);  
```  
  
#### Parameters  
 [in] `pWndParentFrame`  
 A pointer to the parent window of the `CMFCKeyMapDialog` object.  
  
 [in] `bEnablePrint`  
 `TRUE` if the list of accelerator keys can be printed; otherwise, `FALSE`. The default is `FALSE`.  
  
## Remarks  
  
## Example  
 The following example demonstrates how to construct an object of the `CMFCKeyMapDialog` class. This example is part of the [Visual Studio Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#21](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#21)]  
  
## Requirements  
 **Header:** afxkeymapdialog.h  
  
## See Also  
 [CMFCKeyMapDialog Class](../vs140/CMFCKeyMapDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)