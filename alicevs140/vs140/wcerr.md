---
title: "wcerr"
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
ms.assetid: 8b4ca0b7-99a5-45c2-a221-b4e1545b8d32
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wcerr
Specifies the `wcerr` global stream.  
  
## Syntax  
  
```  
extern wostream wcerr;  
```  
  
## Return Value  
 A [wostream](../vs140/wostream.md) object.  
  
## Remarks  
 The object controls unbuffered insertions to the standard error output as a wide stream. Once the object is constructed, the expression `wcerr.`[flags](../vs140/ios_base--flags.md) `&` [unitbuf](../vs140/unitbuf.md) is nonzero.  
  
## Example  
 See [cerr](../vs140/cerr.md) for an example of using `wcerr`.  
  
## Requirements  
 **Header:** <iostream\>  
  
 **Namespace:** std  
  
## See Also  
 [wostream](../vs140/wostream.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)