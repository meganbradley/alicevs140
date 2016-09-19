---
title: "ATLPath::BuildRoot"
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
ms.assetid: b67c4664-b63f-4a26-b8c5-6ad09aae0081
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::BuildRoot
This function is an overloaded wrapper for [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567).  
  
## Syntax  
  
```  
  
      inline char* BuildRoot(  
   char* pszPath,  
   int iDrive   
);  
inline wchar_t* BuildRoot(  
   wchar_t* pszPath,  
   int iDrive   
);  
```  
  
## Remarks  
 See [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567)