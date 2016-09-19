---
title: "nouppercase"
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
ms.assetid: 7da102a7-5654-4aee-9965-6b36b271c8af
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# nouppercase
Specifies that hexadecimal digits and the exponent in scientific notation appear in lowercase.  
  
## Syntax  
  
```  
  
      ios  
      _  
      base& nouppercase(  
   ios_base& _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 A reference to an object of type [ios_base](../vs140/ios_base-Class.md), or to a type that inherits from `ios_base`.  
  
## Return Value  
 A reference to the object from which _*Str* is derived.  
  
## Remarks  
 The manipulator effectively calls `_Str.`[unsetf](../vs140/ios_base--unsetf.md)(`ios_base::uppercase`), and then returns `_Str`.  
  
## Example  
 See [uppercase](../vs140/uppercase.md) for an example of using `nouppercase`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)