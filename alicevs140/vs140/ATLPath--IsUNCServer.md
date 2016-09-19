---
title: "ATLPath::IsUNCServer"
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
ms.assetid: f0f2763d-6918-4610-a66d-04996d2efeaf
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::IsUNCServer
This function is an overloaded wrapper for [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722).  
  
## Syntax  
  
```  
  
      inline BOOL IsUNCServer(  
   const char* pszPath   
);  
inline BOOL IsUNCServer(  
   const wchar_t* pszPath   
);  
```  
  
## Remarks  
 See [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722)