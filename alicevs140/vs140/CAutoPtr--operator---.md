---
title: "CAutoPtr::operator -&gt;"
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
ms.assetid: ec818fcb-166e-4f53-a961-b17774a05f6f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtr::operator -&gt;
The pointer-to-member operator.  
  
## Syntax  
  
```  
  
T * operator ->( ) const throw( );  
  
```  
  
## Return Value  
 Returns the value of the [CAutoPtr::m_p](../vs140/CAutoPtr--m_p.md) data member variable.  
  
## Remarks  
 Use this operator to call a method in a class pointed to by the `CAutoPtr` object. In debug builds, an assertion failure will occur if the `CAutoPtr` points to NULL.  
  
## Example  
 See the example in the [CAutoPtr Overview](../vs140/CAutoPtr-Class.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)