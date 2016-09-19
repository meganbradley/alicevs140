---
title: "CAxDialogImpl::DoModal"
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
ms.assetid: 6e73edec-cf82-4179-95d9-ca18d8814fb3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxDialogImpl::DoModal
Call this method to create a modal dialog box.  
  
## Syntax  
  
```  
  
      INT_PTR DoModal(  
   HWND hWndParent = ::GetActiveWindow( ),  
   LPARAM dwInitParam = NULL   
);  
```  
  
#### Parameters  
 `hWndParent`  
 [in] The handle to the owner window. The default value is the return value of the [GetActiveWindow](http://msdn.microsoft.com/library/windows/desktop/ms646292) Win32 function.  
  
 `dwInitParam`  
 [in] Specifies the value to pass to the dialog box in the `lParam` parameter of the **WM_INITDIALOG** message.  
  
## Return Value  
 If successful, the value of the `nRetCode` parameter specified in the call to [EndDialog](../vs140/CAxDialogImpl--EndDialog.md); otherwise, -1.  
  
## Remarks  
 This dialog box is automatically attached to the `CAxDialogImpl` object.  
  
 To create a modeless dialog box, call [Create](../vs140/CAxDialogImpl--Create.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxDialogImpl Class](../vs140/CAxDialogImpl-Class.md)   
 [CAxDialogImpl::EndDialog](../vs140/CAxDialogImpl--EndDialog.md)   
 [CAxDialogImpl::Create](../vs140/CAxDialogImpl--Create.md)