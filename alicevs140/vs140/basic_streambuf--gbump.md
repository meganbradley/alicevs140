---
title: "basic_streambuf::gbump"
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
ms.assetid: 1ff7c880-1d91-46ab-a4b3-9be9d9b6309f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::gbump
A protected function that adds `_Count` to the next pointer for the input buffer.  
  
## Syntax  
  
```  
  
      void gbump(  
   int _Count  
);  
```  
  
#### Parameters  
 `_Count`  
 The amount by which to advance the pointer.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)