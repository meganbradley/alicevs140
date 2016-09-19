---
title: "CDialogImpl::GetDialogProc"
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
ms.assetid: e9f11f77-4355-4ac4-9532-518be2275745
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialogImpl::GetDialogProc
Returns `DialogProc`, the current dialog box procedure.  
  
## Syntax  
  
```  
  
virtual WNDPROC GetDialogProc( );  
  
```  
  
## Return Value  
 The current dialog box procedure.  
  
## Remarks  
 Override this method to replace the dialog procedure with your own.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDialogImpl Class](../vs140/CDialogImpl-Class.md)   
 [CDialogImpl::DialogProc](../vs140/CDialogImpl--DialogProc.md)   
 [CDialogImpl::OnFinalMessage](../vs140/CDialogImpl--OnFinalMessage.md)