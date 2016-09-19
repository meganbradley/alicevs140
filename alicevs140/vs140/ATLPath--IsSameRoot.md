---
title: "ATLPath::IsSameRoot"
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
ms.assetid: dcdebc4e-eda2-45e4-af8d-5c5bb440481f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::IsSameRoot
This function is an overloaded wrapper for [PathIsSameRoot](http://msdn.microsoft.com/library/windows/desktop/bb773687).  
  
## Syntax  
  
```  
  
      inline BOOL IsSameRoot(  
   const char* pszPath1,  
   const char* pszPath2   
);  
inline BOOL IsSameRoot(  
   const wchar_t* pszPath1,  
   const wchar_t* pszPath2   
);  
```  
  
## Remarks  
 See [PathIsSameRoot](http://msdn.microsoft.com/library/windows/desktop/bb773687) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathIsSameRoot](http://msdn.microsoft.com/library/windows/desktop/bb773687)