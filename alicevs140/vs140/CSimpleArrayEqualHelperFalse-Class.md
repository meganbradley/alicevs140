---
title: "CSimpleArrayEqualHelperFalse Class"
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
ms.assetid: 6918af6f-d23d-49eb-8482-c44272f5ffeb
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArrayEqualHelperFalse Class
This class is a helper for the [CSimpleArray](../vs140/CSimpleArray-Class.md) class.  
  
## Syntax  
  
```  
  
template <class T  
   >   
   class CSimpleArrayEqualHelperFalse  
  
```  
  
#### Parameters  
 `T`  
 A derived class.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleArrayEqualHelperFalse::IsEqual](../vs140/CSimpleArrayEqualHelperFalse--IsEqual.md)|(Static) Returns false.|  
  
## Remarks  
 This traits class is a complement to the `CSimpleArray` class. It always returns false, and in addition, will call `ATLASSERT` with an argument of false if it is ever referenced. In situations where the equality test is not sufficiently defined, this class allows an array containing elements to operate correctly for most methods but fail in a well-defined manner for methods that depend on comparisons such as [CSimpleArray::Find](../vs140/CSimpleArray--Find.md).  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
##  <a name="csimplearrayequalhelperfalse__isequal"></a>  CSimpleArrayEqualHelperFalse::IsEqual  
 Returns false.  
  
```  
  
static bool IsEqual(  
      const T& ,  
      const T&   
   );  
  
```  
  
### Return Value  
 Returns false.  
  
### Remarks  
 This method always returns false, and will call `ATLASSERT` with an argument of false if referenced. The purpose of `CSimpleArrayEqualHelperFalse::IsEqual` is to force methods using comparisons to fail in a well-defined manner when equality tests have not been adequately defined.  
  
## See Also  
 [CSimpleArrayEqualHelper Class](../vs140/CSimpleArrayEqualHelper-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)