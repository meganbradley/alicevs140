---
title: "CWnd::OnTouchInputs"
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
ms.assetid: 75b0ff87-28c6-4b4c-9521-c44a95a8e411
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnTouchInputs
Processes inputs from Windows touch.  
  
## Syntax  
  
```  
virtual BOOL OnTouchInputs(  
   UINT nInputsCount,  
   PTOUCHINPUT pInputs  
);  
```  
  
#### Parameters  
 `nInputsCount`  
 Total number of Windows touch inputs.  
  
 `pInputs`  
 Array of TOUCHINPUT.  
  
## Return Value  
 `TRUE` if application processes Windows touch inputs; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)