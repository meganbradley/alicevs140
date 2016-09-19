---
title: "fpos::operator-"
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
ms.assetid: c640f7a5-0e5a-421f-aa3b-d88d9e86d8fc
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fpos::operator-
Decrements a file-position indicator.  
  
## Syntax  
  
```  
streamoff operator-(  
   const fpos<Statetype>& _Right  
) const;  
fpos<Statetype> operator-(  
   streamoff _Off  
) const;  
```  
  
#### Parameters  
 `_Right`  
 File position.  
  
 `_Off`  
 Stream offset.  
  
## Return Value  
 The first member function returns **(streamoff)\*this - (streamoff)**`_Right`. The second member function returns **fpos(\*this) -=** `_Off`.  
  
## Example  
 See [operator!=](../vs140/fpos--operator!=.md) for a sample of using `operator-`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [fpos Class](../vs140/fpos-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)