---
title: "basic_streambuf::setg"
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
ms.assetid: 1c5dd011-dd7c-4808-9688-ee75d0f1c84b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::setg
A protected function that stores _*Gbeg* in the beginning pointer, `_Gnext` in the next pointer, and `_Gend` in the end pointer for the input buffer.  
  
## Syntax  
  
```  
  
      void setg(  
   char_type *_Gbeg,  
   char_type *_Gnext,  
   char_type *_Gend  
);  
```  
  
#### Parameters  
 *_Gbeg*  
 A pointer to the beginning of the buffer.  
  
 `_Gnext`  
 A pointer to somewhere in the middle of the buffer.  
  
 `_Gend`  
 A pointer to the end of the buffer.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)