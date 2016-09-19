---
title: "com::ptr"
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
ms.topic: reference
ms.assetid: ee302e3c-8fed-4875-a372-2e55003718d3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# com::ptr
A wrapper for a COM object that can be used as a member of a CLR class. The wrapper also automates lifetime management of the COM object, releasing owned references on the object when its destructor is called. Analogous to [CComPtr](../vs140/CComPtr-Class.md).  
  
## Syntax  
  
```  
#include <msclr\com\ptr.h>  
```  
  
## Remarks  
 [com::ptr Class](../vs140/com--ptr-Class.md) is defined in the <msclr\com\ptr.h> file.  
  
## See Also  
 [C++ Support Library](../vs140/C---Support-Library.md)