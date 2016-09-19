---
title: "showpoint"
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
ms.assetid: 1a5f8235-2bb2-4b3c-b9b8-d76e75046953
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# showpoint
Displays the whole-number part of a floating-point number and digits to the right of the decimal point even when the fractional part is zero.  
  
## Syntax  
  
```  
  
      ios  
      _  
      base& showpoint(  
   ios_base& _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 A reference to an object of type [ios_base](../vs140/ios_base-Class.md), or to a type that inherits from `ios_base`.  
  
## Return Value  
 A reference to the object from which _*Str* is derived.  
  
## Remarks  
 By default, [noshowpoint](../vs140/noshowpoint.md) is in effect.  
  
 The manipulator effectively calls `_Str.`[setf](../vs140/ios_base--setf.md)(`ios_base::showpoint`), and then returns `_Str`.  
  
## Example  
 See [noshowpoint](../vs140/noshowpoint.md) for an example of using `showpoint`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)