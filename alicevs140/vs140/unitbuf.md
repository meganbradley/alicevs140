---
title: "unitbuf"
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
ms.assetid: 4732c788-d891-4ff0-83ec-3036527acd81
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unitbuf
Causes output to be processed when the buffer is not empty.  
  
## Syntax  
  
```  
  
      ios  
      _  
      base& unitbuf(  
   ios_base& _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 A reference to an object of type [ios_base](../vs140/ios_base-Class.md), or to a type that inherits from `ios_base`.  
  
## Return Value  
 A reference to the object from which `_Str` is derived.  
  
## Remarks  
 Note that `endl` also flushes the buffer.  
  
 [nounitbuf](../vs140/nounitbuf.md) is in effect by default.  
  
 The manipulator effectively calls `_Str.`[setf](../vs140/ios_base--setf.md)([ios_base::unitbuf](../vs140/ios_base--fmtflags.md)), and then returns `_Str`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)