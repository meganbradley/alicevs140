---
title: "no_smart_pointers"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d69dd71e-08a8-4446-a3d0-a062dc29cb17
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# no_smart_pointers
**C++ Specific**  
  
 Suppresses the creation of smart pointers for all interfaces in the type library.  
  
## Syntax  
  
```  
no_smart_pointers  
```  
  
## Remarks  
 By default, when you use `#import`, you get a smart pointer declaration for all interfaces in the type library. These smart pointers are of type [_com_ptr_t Class](../vs140/_com_ptr_t-Class.md).  
  
 **END C++ Specific**  
  
## See Also  
 [#import Attributes](../vs140/#import-Attributes--C---.md)   
 [The #import Directive](../vs140/#import-Directive--C---.md)