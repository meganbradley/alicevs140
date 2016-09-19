---
title: "CCommonDialog::CCommonDialog"
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
ms.assetid: bfa36e22-5aea-4874-933c-8ff5a0529be8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommonDialog::CCommonDialog
Constructs a `CCommonDialog` object.  
  
## Syntax  
  
```  
  
      explicit CCommonDialog(  
   CWnd* pParentWnd   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 Points to the parent or owner window object (of type [CWnd](../vs140/CWnd-Class.md)) to which the dialog object belongs. If it is **NULL**, the dialog object's parent window is set to the main application window.  
  
## Remarks  
 See [CDialog::CDialog](../vs140/CDialog--CDialog.md) for complete information.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CCommonDialog Class](../vs140/CCommonDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::CDialog](../vs140/CDialog--CDialog.md)