---
title: "CDHtmlDialog::CDHtmlDialog"
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
ms.assetid: 8438979e-fcd9-4a3b-9b53-7c0321745c8d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::CDHtmlDialog
Constructs a resource-based dynamic HTML dialog box.  
  
## Syntax  
  
```  
  
      CDHtmlDialog( );   
CDHtmlDialog(  
   LPCTSTR lpszTemplateName,  
   LPCTSTR szHtmlResID,  
   CWnd *pParentWnd = NULL   
);  
CDHtmlDialog(  
   UINT nIDTemplate,  
   UINT nHtmlResID = 0,  
   CWnd *pParentWnd = NULL   
);  
```  
  
#### Parameters  
 `lpszTemplateName`  
 The null-terminated string that is the name of a dialog-box template resource.  
  
 `szHtmlResID`  
 The null-terminated string that is the name of an HTML resource.  
  
 `pParentWnd`  
 A pointer to the parent or owner window object (of type [CWnd](../vs140/CWnd-Class.md)) to which the dialog object belongs. If it is **NULL**, the dialog object's parent window is set to the main application window.  
  
 `nIDTemplate`  
 Contains the ID number of a dialog-box template resource.  
  
 `nHtmlResID`  
 Contains the ID number of an HTML resource.  
  
## Remarks  
 The second form of the constructor provides access to the dialog resource through the template name. The third form of the constructor provides access to the dialog resource through the ID of the resource template. Usually, the ID begins with the **IDD_** prefix.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::LoadFromResource](../vs140/CDHtmlDialog--LoadFromResource.md)