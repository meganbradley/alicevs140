---
title: "ios_base::ios_base"
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
ms.assetid: 0c33c52e-a94d-4c91-a1f2-964a7ba30592
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::ios_base
Constructs ios_base objects.  
  
## Syntax  
  
```  
  
ios  
_  
base( );  
  
```  
  
## Remarks  
 The (protected) constructor does nothing. A later call to **basic_ios::**[init](../vs140/basic_ios--init.md) must initialize the object before it can be safely destroyed. Thus, the only safe use for class ios_base is as a base class for template class [basic_ios](../vs140/basic_ios-Class.md).  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)