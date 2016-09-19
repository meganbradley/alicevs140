---
title: "ATLPath::IsRelative"
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
ms.assetid: 639b792a-1692-4cc5-8abf-07cf0fe0d46b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::IsRelative
This function is an overloaded wrapper for [PathIsRelative](http://msdn.microsoft.com/library/windows/desktop/bb773660).  
  
## Syntax  
  
```  
  
      inline BOOL IsRelative(  
   const char* pszPath   
);  
inline BOOL IsRelative(  
   const wchar_t* pszPath   
);  
```  
  
## Remarks  
 See [PathIsRelative](http://msdn.microsoft.com/library/windows/desktop/bb773660) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathIsRelative](http://msdn.microsoft.com/library/windows/desktop/bb773660)