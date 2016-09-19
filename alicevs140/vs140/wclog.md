---
title: "wclog"
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
ms.assetid: 511e20ad-1712-4acc-a894-6243e749f07a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# wclog
Specifies the `wclog` global stream.  
  
## Syntax  
  
```  
extern wostream wclog;  
```  
  
## Return Value  
 A [wostream](../vs140/wostream.md) object.  
  
## Remarks  
 The object controls buffered insertions to the standard error output as a wide stream.  
  
## Example  
 See [cerr](../vs140/cerr.md) for an example of using `wclog`.  
  
## Requirements  
 **Header:** <iostream\>  
  
 **Namespace:** std  
  
## See Also  
 [wostream](../vs140/wostream.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)