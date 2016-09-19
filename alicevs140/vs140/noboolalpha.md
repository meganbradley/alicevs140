---
title: "noboolalpha"
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
ms.assetid: b36f6a55-49ec-4398-af3d-b0dc9c8bd5e5
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# noboolalpha
Specifies that variables of type [bool](../vs140/bool--C---.md) appear as 1 or 0 in the stream.  
  
## Syntax  
  
```  
  
      ios  
      _  
      base& noboolalpha(  
   ios_base& _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 A reference to an object of type [ios_base](../vs140/ios_base-Class.md), or to a type that inherits from `ios_base`.  
  
## Return Value  
 A reference to the object from which _*Str* is derived.  
  
## Remarks  
 By default, `noboolalpha` is in effect.  
  
 `noboolalpha` effectively calls `_Str.`[unsetf](../vs140/ios_base--unsetf.md)(`ios_base::boolalpha`), and then returns `_Str`.  
  
 [boolalpha](../vs140/boolalpha.md) reverses the effect of `noboolalpha`.  
  
## Example  
 See [boolalpha](../vs140/boolalpha.md) for an example of using `noboolalpha`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)