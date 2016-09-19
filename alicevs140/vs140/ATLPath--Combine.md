---
title: "ATLPath::Combine"
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
ms.assetid: 607beb7e-a8e7-40e2-a8a4-af614ce0843f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::Combine
This function is an overloaded wrapper for [PathCombine](http://msdn.microsoft.com/library/windows/desktop/bb773571).  
  
## Syntax  
  
```  
  
      inline char* Combine(  
   char* pszDest,  
   const char* pszDir,  
   const char* pszFile   
);  
inline wchar_t* Combine(  
   wchar_t* pszDest,  
   const wchar_t* pszDir,  
   const wchar_t* pszFile   
);  
```  
  
## Remarks  
 See [PathCombine](http://msdn.microsoft.com/library/windows/desktop/bb773571) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathCombine](http://msdn.microsoft.com/library/windows/desktop/bb773571)