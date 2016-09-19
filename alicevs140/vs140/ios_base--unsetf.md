---
title: "ios_base::unsetf"
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
ms.assetid: c363bae8-62f7-40d5-8453-f5210e948668
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::unsetf
Causes the specified flags to be off.  
  
## Syntax  
  
```  
  
      void unsetf(  
   fmtflags _Mask  
);  
```  
  
#### Parameters  
 `_Mask`  
 The flags that you want off.  
  
## Remarks  
 The member function effectively calls [flags](../vs140/ios_base--flags.md)(`~`*_Mask* **& flags**) (clear selected bits).  
  
## Example  
 See [ios_base::setf](../vs140/ios_base--setf.md) for a sample of using `unsetf`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)