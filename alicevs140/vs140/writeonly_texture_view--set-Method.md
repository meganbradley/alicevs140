---
title: "writeonly_texture_view::set Method"
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
ms.topic: article
ms.assetid: 542fbc39-b9f4-4b6b-95a8-fd6581116a7f
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# writeonly_texture_view::set Method
Sets the value of the element at the specified index.  
  
## Syntax  
  
```  
void set(  
   const index<_Rank>& _Index,  
   const value_type& _Value                       
) const restrict(amp);  
```  
  
#### Parameters  
 `_Index`  
 The index of the element.  
  
 `_Value`  
 The new value of the element.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [writeonly_texture_view Class](../vs140/writeonly_texture_view-Class.md)