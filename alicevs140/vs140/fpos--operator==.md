---
title: "fpos::operator=="
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
ms.assetid: a8bb86d8-e0a4-4781-b754-06fbc2a46faa
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fpos::operator==
Tests file-position indicators for equality.  
  
## Syntax  
  
```  
bool operator==(  
    const fpos<Statetype>& _Right  
) const;  
```  
  
#### Parameters  
 `_Right`  
 The file-position indicator against which to compare.  
  
## Return Value  
 **true** if the file-position indicators are equal; otherwise **false**.  
  
## Remarks  
 The member function returns **(streamoff)\*this == (streamoff)**`_Right`.  
  
## Example  
 See [operator!=](../vs140/fpos--operator!=.md) for a sample of using `operator+=`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [fpos Class](../vs140/fpos-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)