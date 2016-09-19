---
title: "ATLPath::Canonicalize"
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
ms.assetid: e3bf7785-f1d9-4299-83c0-6ede590e1ae6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::Canonicalize
This function is an overloaded wrapper for [PathCanonicalize](http://msdn.microsoft.com/library/windows/desktop/bb773569).  
  
## Syntax  
  
```  
  
      inline BOOL Canonicalize(  
   char* pszDest,  
   const char* pszSrc   
);  
inline BOOL Canonicalize(  
   wchar_t* pszDest,  
   const wchar_t* pszSrc   
);  
```  
  
## Remarks  
 See [PathCanonicalize](http://msdn.microsoft.com/library/windows/desktop/bb773569) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathCanonicalize](http://msdn.microsoft.com/library/windows/desktop/bb773569)