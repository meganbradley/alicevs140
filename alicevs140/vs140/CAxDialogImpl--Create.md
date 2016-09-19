---
title: "CAxDialogImpl::Create"
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
ms.assetid: 4d32454c-570a-4601-8926-e6c70d569091
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxDialogImpl::Create
Call this method to create a modeless dialog box.  
  
## Syntax  
  
```  
  
      HWND Create(  
   HWND hWndParent,  
   LPARAM dwInitParam = NULL   
);  
HWND Create(  
   HWND hWndParent,  
   RECT&,  
   LPARAM dwInitParam = NULL   
);  
```  
  
#### Parameters  
 `hWndParent`  
 [in] The handle to the owner window.  
  
 `dwInitParam`  
 [in] Specifies the value to pass to the dialog box in the `lParam` parameter of the **WM_INITDIALOG** message.  
  
 **RECT&**  
 This parameter is not used. This parameter is passed in by `CComControl`.  
  
## Return Value  
 The handle to the newly created dialog box.  
  
## Remarks  
 This dialog box is automatically attached to the `CAxDialogImpl` object. To create a modal dialog box, call [DoModal](../vs140/CAxDialogImpl--DoModal.md).  
  
 The second override is provided only so dialog boxes can be used with [CComControl](../vs140/CComControl-Class.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxDialogImpl Class](../vs140/CAxDialogImpl-Class.md)   
 [CAxDialogImpl::DestroyWindow](../vs140/CAxDialogImpl--DestroyWindow.md)   
 [CAxDialogImpl::DoModal](../vs140/CAxDialogImpl--DoModal.md)