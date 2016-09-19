---
title: "CColorDialog::CColorDialog"
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
ms.assetid: 2ac0bd98-885a-41c0-8c06-da90ca248ad2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CColorDialog::CColorDialog
Constructs a `CColorDialog` object.  
  
## Syntax  
  
```  
  
      CColorDialog(  
   COLORREF clrInit = 0,  
   DWORD dwFlags = 0,  
   CWnd* pParentWnd = NULL   
);  
```  
  
#### Parameters  
 *clrInit*  
 The default color selection. If no value is specified, the default is RGB(0,0,0) (black).  
  
 `dwFlags`  
 A set of flags that customize the function and appearance of the dialog box. For more information, see the [CHOOSECOLOR](http://msdn.microsoft.com/library/windows/desktop/ms646830) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pParentWnd`  
 A pointer to the dialog box's parent or owner window.  
  
## Example  
 [!CODE [NVC_MFCDocView#49](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#49)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CColorDialog Class](../vs140/CColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)