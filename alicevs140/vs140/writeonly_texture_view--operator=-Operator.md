---
title: "writeonly_texture_view::operator= Operator"
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
ms.assetid: 03635f51-dbf4-4449-aaf4-74378a9a889f
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# writeonly_texture_view::operator= Operator
Copies the specified [writeonly_texture_view](../vs140/writeonly_texture_view-Class.md) object to this one.  
  
## Syntax  
  
```  
writeonly_texture_view<_Value_type, _Rank>& operator=(  
   const writeonly_texture_view<_Value_type, _Rank>& _Other  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Other`  
 [writeonly_texture_view](../vs140/writeonly_texture_view-Class.md) object to copy from.  
  
## Return Value  
 A reference to this [writeonly_texture_view](../vs140/writeonly_texture_view-Class.md) object.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [writeonly_texture_view Class](../vs140/writeonly_texture_view-Class.md)