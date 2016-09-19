---
title: "ATLPath::AddExtension"
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
ms.assetid: 3bc95212-332f-458e-a841-0792b4805f46
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::AddExtension
This function is an overloaded wrapper for [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563).  
  
## Syntax  
  
```  
  
      inline BOOL AddExtension(  
   char* pszPath,  
   const char* pszExtension   
);  
inline BOOL AddExtension(  
   wchar_t* pszPath,  
   const wchar_t* pszExtension   
);  
```  
  
## Remarks  
 See [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563)