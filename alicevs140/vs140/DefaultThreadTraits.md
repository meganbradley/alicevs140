---
title: "DefaultThreadTraits"
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
ms.assetid: 0c43d8c7-b13d-4827-9d08-5c02852e22a7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DefaultThreadTraits
The default thread traits class.  
  
## Syntax  
  
```  
  
      #if defined(_MT)  
   typedef CRTThreadTraits DefaultThreadTraits;  
#else  
   typedef Win32ThreadTraits DefaultThreadTraits;  
#endif  
```  
  
## Remarks  
 If the current project uses the multithreaded CRT, `DefaultThreadTraits` is defined as [CRTThreadTraits](../vs140/CRTThreadTraits-Class.md). Otherwise, [Win32ThreadTraits](../vs140/Win32ThreadTraits-Class.md) is used.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Typedefs](../vs140/ATL-Typedefs.md)