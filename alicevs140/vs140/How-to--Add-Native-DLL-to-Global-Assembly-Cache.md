---
title: "How to: Add Native DLL to Global Assembly Cache"
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
ms.topic: get-started-article
ms.assetid: 25e8d78a-b197-4269-b4e9-237a544ab3c8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Add Native DLL to Global Assembly Cache
You can put a native DLL (not COM) into the Global Assembly Cache.  
  
## Example  
 **/ASSEMBLYLINKRESOURCE** lets you embed a native DLL in an assembly.  
  
 For more information, see [/ASSEMBLYLINKRESOURCE (Link to .NET Framework Resource)](../Topic/-ASSEMBLYLINKRESOURCE%20\(Link%20to%20.NET%20Framework%20Resource\).md).  
  
```  
/ASSEMBLYLINKRESOURCE:MyComponent.dll  
```  
  
## See Also  
 [Using C++ Interop Features](../vs140/Using-C---Interop--Implicit-PInvoke-.md)