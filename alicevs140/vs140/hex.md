---
title: "hex"
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
ms.assetid: 227470c8-3e0d-42da-b9ad-f37ea372e5bc
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hex
Specifies that integer variables shall appear in base 16 notation.  
  
## Syntax  
  
```  
  
      ios  
      _  
      base& hex(  
   ios_base& _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 A reference to an object of type [ios_base](../vs140/ios_base-Class.md), or to a type that inherits from `ios_base`.  
  
## Return Value  
 A reference to the object from which _*Str* is derived.  
  
## Remarks  
 By default, integer variables are displayed in base 10 notation. [dec](../vs140/dec.md) and [oct](../vs140/oct---ios--.md) also change the way integer variables appear.  
  
 The manipulator effectively calls `_Str`**.**[setf](../vs140/ios_base--setf.md)(`ios_base::hex`, **ios_base::basefield**), and then returns `_Str`.  
  
## Example  
 See [dec](../vs140/dec.md) for an example of how to use **hex**.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)