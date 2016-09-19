---
title: "CDialogImpl::EndDialog"
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
ms.assetid: c85c7a6e-0b87-48b0-bf62-be8d23cd0b1a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialogImpl::EndDialog
Destroys a modal dialog box.  
  
## Syntax  
  
```  
  
      BOOL EndDialog(  
   int nRetCode   
);  
```  
  
#### Parameters  
 `nRetCode`  
 [in] The value to be returned by [CDialogImpl::DoModal](../vs140/CDialogImpl--DoModal.md).  
  
## Return Value  
 **TRUE** if the dialog box is destroyed; otherwise, **FALSE**.  
  
## Remarks  
 `EndDialog` must be called through the dialog procedure. After the dialog box is destroyed, Windows uses the value of `nRetCode` as the return value for `DoModal`, which created the dialog box.  
  
> [!NOTE]
>  Do not call `EndDialog` to destroy a modeless dialog box. Call [CWindow::DestroyWindow](../vs140/CWindow--DestroyWindow.md) instead.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDialogImpl Class](../vs140/CDialogImpl-Class.md)   
 [CDialogImpl::DialogProc](../vs140/CDialogImpl--DialogProc.md)