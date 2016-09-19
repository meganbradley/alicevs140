---
title: "ATLPath::IsDirectory"
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
ms.assetid: d196d0dd-20c2-46d0-9cbe-b2ed211cafcc
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::IsDirectory
This function is an overloaded wrapper for [PathIsDirectory](http://msdn.microsoft.com/library/windows/desktop/bb773621).  
  
## Syntax  
  
```  
  
      inline BOOL IsDirectory(  
   const char* pszPath   
);  
inline BOOL IsDirectory(  
   const wchar_t* pszPath   
);  
```  
  
## Remarks  
 See [PathIsDirectory](http://msdn.microsoft.com/library/windows/desktop/bb773621) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathIsDirectory](http://msdn.microsoft.com/library/windows/desktop/bb773621)