---
title: "ATLPath::MatchSpec"
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
ms.assetid: ad435b5b-5267-4718-94fa-88e5211edefd
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::MatchSpec
This function is an overloaded wrapper for [PathMatchSpec](http://msdn.microsoft.com/library/windows/desktop/bb773727).  
  
## Syntax  
  
```  
  
      inline BOOL MatchSpec(  
   const char* pszPath,  
   const char* pszSpec   
);  
inline BOOL MatchSpec(  
   const wchar_t* pszPath,  
   const wchar_t* pszSpec   
);  
```  
  
## Remarks  
 See [PathMatchSpec](http://msdn.microsoft.com/library/windows/desktop/bb773727) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathMatchSpec](http://msdn.microsoft.com/library/windows/desktop/bb773727)