---
title: "CAxDialogImpl::DestroyWindow"
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
ms.assetid: db769308-a5f3-4c71-981b-9d3fce14abdc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxDialogImpl::DestroyWindow
Call this method to destroy a modeless dialog box.  
  
## Syntax  
  
```  
  
BOOL DestroyWindow( );  
  
```  
  
## Return Value  
 TRUE if the window is successfully destroyed; otherwise FALSE.  
  
## Remarks  
 Do not call `DestroyWindow` to destroy a modal dialog box. Call [EndDialog](../vs140/CAxDialogImpl--EndDialog.md) instead.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxDialogImpl Class](../vs140/CAxDialogImpl-Class.md)   
 [DestroyWindow](http://msdn.microsoft.com/library/windows/desktop/ms632682)