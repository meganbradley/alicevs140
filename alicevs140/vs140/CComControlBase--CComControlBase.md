---
title: "CComControlBase::CComControlBase"
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
ms.assetid: cdfacebc-8d90-4d0e-973c-b953640d149c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::CComControlBase
The constructor.  
  
## Syntax  
  
```  
  
      CComControlBase(  
   HWND& h   
);  
```  
  
#### Parameters  
 `h`  
 The handle to the window associated with the control.  
  
## Remarks  
 Initializes the control size to 5080X5080 HIMETRIC units (2"X2") and initializes the `CComControlBase` data member values to **NULL** or **FALSE**.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::~CComControlBase](../vs140/CComControlBase--~CComControlBase.md)