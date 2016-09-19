---
title: "texture_view::get Method"
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
ms.assetid: 8b4349c7-23fb-44be-b3f5-fad245e390e7
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# texture_view::get Method
Gets the value of the element at the specified index.  
  
## Syntax  
  
```  
const value_type get(  
   const index<_Rank>& _Index  
) const restrict(amp);  
  
value_type get(  
   const index<_Rank>& _Index,  
   unsigned int _Mip_level = 0  
) const restrict(amp);  
```  
  
#### Parameters  
 `_Index`  
 The index of the element to get, possibly multi-dimensional.  
  
 `_Mip_level`  
 The mipmap level from which we should get the value. The default value 0 represents the most detailed mipmap level.  
  
## Return Value  
 The value of the element.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** concurrency::graphics  
  
## See Also  
 [texture_view Class](../vs140/texture_view-Class.md)