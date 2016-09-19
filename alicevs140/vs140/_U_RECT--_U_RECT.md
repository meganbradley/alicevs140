---
title: "_U_RECT::_U_RECT"
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
ms.assetid: fcc5ddc4-0c98-417c-9c1a-c6dafcdd8c06
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _U_RECT::_U_RECT
The address of the reference argument is stored in the class's single data member, [m_lpRect](../vs140/_U_RECT--m_lpRect.md).  
  
## Syntax  
  
```  
  
      _U_RECT(  
   RECT& rc   
);  
_U_RECT(  
   LPRECT lpRect   
);  
```  
  
#### Parameters  
 `rc`  
 A `RECT` reference.  
  
 `lpRect`  
 A `RECT` pointer.  
  
## Remarks  
 The argument to the pointer constructor is stored directly without conversion.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [_U_RECT Class](../vs140/_U_RECT-Class.md)   
 [_U_RECT::m_lpRect](../vs140/_U_RECT--m_lpRect.md)