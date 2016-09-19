---
title: "wcout"
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
ms.assetid: c18cc19b-cd7f-4d5f-8fa9-e2cac4df061c
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wcout
Specifies the `wcout` global stream.  
  
## Syntax  
  
```  
extern wostream wcout;  
```  
  
## Return Value  
 A [wostream](../vs140/wostream.md) object.  
  
## Remarks  
 The object controls insertions to the standard output as a wide stream.  
  
## Example  
 See [cerr](../vs140/cerr.md) for an example of using `wcout`.  
  
 `CString` instances in a `wcout` statement must be cast to `const wchar_t*`, as shown in the following example.  
  
```  
  
      CString cs("meow");  
    wcout << (const wchar_t*) cs << endl;  
```  
  
 For more information, see [Basic CString Operations](../vs140/Basic-CString-Operations.md).  
  
## Requirements  
 **Header:** <iostream\>  
  
 **Namespace:** std  
  
## See Also  
 [wostream](../vs140/wostream.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)