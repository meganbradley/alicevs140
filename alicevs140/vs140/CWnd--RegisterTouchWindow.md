---
title: "CWnd::RegisterTouchWindow"
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
ms.assetid: 52d3ddc4-b2f1-4610-96c5-cbfadb78d5e2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::RegisterTouchWindow
Registers or unregisters Windows touch support.  
  
## Syntax  
  
```  
BOOL RegisterTouchWindow(  
   BOOL bRegister = TRUE,  
   ULONG ulFlags = 0  
);  
```  
  
#### Parameters  
 `bRegister`  
 `TRUE` indicates register Windows touch support; `FALSE` otherwise.  
  
 `ulFlags`  
 A set of bit flags that specify optional modifications. This field may contain 0 or one of the following values: TWF_FINETOUCH, TWF_WANTPALM.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)