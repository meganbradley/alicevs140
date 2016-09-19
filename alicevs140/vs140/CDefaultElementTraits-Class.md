---
title: "CDefaultElementTraits Class"
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
ms.assetid: ac5ee610-7957-4b7c-92b6-38ff72e4118e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDefaultElementTraits Class
This class provides default methods and functions for a collection class.  
  
## Syntax  
  
```  
  
template<  
      typename  T>  
   class CDefaultElementTraits : public CElementTraitsBase<  T  
    >,  
      public CDefaultHashTraits<  T  
    >,  
      public CDefaultCompareTraits<  T  
    >  
  
```  
  
#### Parameters  
 `T`  
 The type of data to be stored in the collection.  
  
## Remarks  
 This class provides default static functions and methods for moving, copying, comparing, and hashing elements stored in a collection class object. This class derives its functions and methods from [CElementTraitsBase](../vs140/CElementTraitsBase-Class.md), [CDefaultHashTraits](../vs140/CDefaultHashTraits-Class.md), and [CDefaultCompareTraits](../vs140/CDefaultCompareTraits-Class.md), and is utilized by [CElementTraits](../vs140/CElementTraits-Class.md), [CPrimitiveElementTraits](../vs140/CPrimitiveElementTraits-Class.md), and [CHeapPtrElementTraits](../vs140/CHeapPtrElementTraits-Class.md).  
  
 For more information, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)