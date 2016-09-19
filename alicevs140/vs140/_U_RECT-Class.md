---
title: "_U_RECT Class"
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
ms.assetid: 5f880a2d-09cf-4327-bf32-a3519c4dcd63
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _U_RECT Class
This argument adapter class allows either `RECT` pointers or references to be passed to a function that is implemented in terms of pointers.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class _U_RECT  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[_U_RECT::_U_RECT](../vs140/_U_RECT--_U_RECT.md)|The constructor.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[_U_RECT::m_lpRect](../vs140/_U_RECT--m_lpRect.md)|Pointer to a `RECT`.|  
  
## Remarks  
 The class defines two constructor overloads: one accepts a **RECT&** argument and the other accepts an `LPRECT` argument. The first constructor stores the address of the reference argument in the class's single data member, [m_lpRect](../vs140/_U_RECT--m_lpRect.md). The argument to the pointer constructor is stored directly without conversion.  
  
## Requirements  
 **Header:** atlwin.h  
  
##  <a name="_u_rect__m_lprect"></a>  _U_RECT::m_lpRect  
 The class holds the value passed to either of its constructors as a public `LPRECT` data member.  
  
```  
  
LPRECT m_lpRect;  
  
```  
  
##  <a name="_u_rect___u_rect"></a>  _U_RECT::_U_RECT  
 The address of the reference argument is stored in the class's single data member, [m_lpRect](../vs140/_U_RECT--m_lpRect.md).  
  
```  
  
_U_RECT(  
      RECT&  rc  
   );  
   _U_RECT(  
      LPRECT  lpRect  
   );  
  
```  
  
### Parameters  
 `rc`  
 A `RECT` reference.  
  
 `lpRect`  
 A `RECT` pointer.  
  
### Remarks  
 The argument to the pointer constructor is stored directly without conversion.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)