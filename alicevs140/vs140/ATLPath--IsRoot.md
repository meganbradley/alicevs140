---
title: "ATLPath::IsRoot"
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
ms.assetid: b7346e99-3eac-4e2e-9f84-ddb6c45d0ed6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::IsRoot
This function is an overloaded wrapper for [PathIsRoot](http://msdn.microsoft.com/library/windows/desktop/bb773674).  
  
## Syntax  
  
```  
  
      inline BOOL IsRoot(  
   const char* pszPath   
);  
inline BOOL IsRoot(  
   const wchar_t* pszPath   
);  
```  
  
## Remarks  
 See [PathIsRoot](http://msdn.microsoft.com/library/windows/desktop/bb773674) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathIsRoot](http://msdn.microsoft.com/library/windows/desktop/bb773674)