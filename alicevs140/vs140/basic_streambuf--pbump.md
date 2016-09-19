---
title: "basic_streambuf::pbump"
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
ms.assetid: 8ea64230-cd31-4f3b-a24c-97e87af5ba41
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::pbump
A protected function that adds `_Count` to the next pointer for the output buffer.  
  
## Syntax  
  
```  
  
      void pbump(  
   int _Count  
);  
```  
  
#### Parameters  
 `_Count`  
 The number of characters by which to move the write position forward.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)