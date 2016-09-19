---
title: "External Linkage"
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
ms.assetid: a6f8ea69-b405-4cdd-bf12-ad5462b73183
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# External Linkage
If the first declaration at file-scope level for an identifier does not use the **static** storage-class specifier, the object has external linkage.  
  
 If the declaration of an identifier for a function has no *storage-class-specifier*, its linkage is determined exactly as if it were declared with the *storage-class-specifier* `extern`. If the declaration of an identifier for an object has file scope and no *storage-class-specifier*, its linkage is external.  
  
 An identifier's name with external linkage designates the same function or data object as does any other declaration for the same name with external linkage. The two declarations can be in the same translation unit or in different translation units. If the object or function also has global lifetime, the object or function is shared by the entire program.  
  
## See Also  
 [Using extern to Specify Linkage](../vs140/Using-extern-to-Specify-Linkage.md)