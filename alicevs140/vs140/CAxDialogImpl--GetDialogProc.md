---
title: "CAxDialogImpl::GetDialogProc"
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
ms.assetid: 448020a7-a398-4ff2-93dd-42fb08cf766c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxDialogImpl::GetDialogProc
Call this method to get a pointer to the `DialogProc` callback function.  
  
## Syntax  
  
```  
  
virtual DLGPROC GetDialogProc( );  
  
```  
  
## Return Value  
 Returns a pointer to the `DialogProc` callback function.  
  
## Remarks  
 The `DialogProc` function is an application-defined callback function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxDialogImpl Class](../vs140/CAxDialogImpl-Class.md)