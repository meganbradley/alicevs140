---
title: "rename_namespace"
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
ms.assetid: 45006d2b-36cd-4bec-98b9-3b8ec45299e3
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rename_namespace
**C++ Specific**  
  
 Renames the namespace that contains the contents of the type library.  
  
## Syntax  
  
```  
rename_namespace("NewName")  
```  
  
#### Parameters  
 `NewName`  
 The new name of the namespace.  
  
## Remarks  
 It takes a single argument, *NewName*, which specifies the new name for the namespace.  
  
 To remove the namespace, use the [no_namespace](../vs140/no_namespace.md) attribute instead.  
  
 **END C++ Specific**  
  
## See Also  
 [#import Attributes](../vs140/#import-Attributes--C---.md)   
 [The #import Directive](../vs140/#import-Directive--C---.md)