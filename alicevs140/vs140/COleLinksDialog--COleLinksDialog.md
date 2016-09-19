---
title: "COleLinksDialog::COleLinksDialog"
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
ms.assetid: d3831cb1-5a3c-4f6e-84c6-83678bbdcf80
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleLinksDialog::COleLinksDialog
Constructs a `COleLinksDialog` object.  
  
## Syntax  
  
```  
  
      COleLinksDialog (  
   COleDocument* pDoc,  
   CView* pView,  
   DWORD dwFlags = 0,  
   CWnd* pParentWnd = NULL   
);  
```  
  
#### Parameters  
 `pDoc`  
 Points to the OLE document that contains the links to be edited.  
  
 `pView`  
 Points to the current view on `pDoc`.  
  
 `dwFlags`  
 Creation flag, which contains either 0 or **ELF_SHOWHELP** to specify whether the Help button will be displayed when the dialog box is displayed.  
  
 `pParentWnd`  
 Points to the parent or owner window object (of type `CWnd`) to which the dialog object belongs. If it is **NULL**, the parent window of the dialog box is set to the main application window.  
  
## Remarks  
 This function constructs only a `COleLinksDialog` object. To display the dialog box, call the [DoModal](../vs140/COleLinksDialog--DoModal.md) function.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleLinksDialog Class](../vs140/COleLinksDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [COleLinksDialog::DoModal](../vs140/COleLinksDialog--DoModal.md)   
 [CView Class](../vs140/CView-Class.md)   
 [CWnd Class](../vs140/CWnd-Class.md)