---
title: "CComControlBase::~CComControlBase"
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
ms.assetid: 8ab1566e-7f3e-4052-80bc-3f0d38afc4f6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::~CComControlBase
The destructor.  
  
## Syntax  
  
```  
  
~CComControlBase( );  
  
```  
  
## Remarks  
 If the control is windowed, `~CComControlBase` destroys it by calling [DestroyWindow](http://msdn.microsoft.com/library/windows/desktop/ms632682).  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::CComControlBase](../vs140/CComControlBase--CComControlBase.md)