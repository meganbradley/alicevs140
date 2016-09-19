---
title: "WeakRef::operator&amp; Operator"
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
ms.assetid: 900afb73-3801-4d08-9b41-2e6a62011ccd
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WeakRef::operator&amp; Operator
Returns a ComPtrRef object that represents the current WeakRef object.  
  
## Syntax  
  
```cpp  
Details::ComPtrRef<WeakRef> operator&() throw()  
```  
  
## Return Value  
 A ComPtrRef object that represents the current WeakRef object.  
  
## Remarks  
 This is an internal helper operator that is not meant to be used in your code.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WeakRef Class](../vs140/WeakRef-Class.md)