---
title: "ATLPath::CommonPrefix"
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
ms.assetid: e5a89a44-9a54-43bc-8d77-77561a0d1453
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::CommonPrefix
This function is an overloaded wrapper for [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574).  
  
## Syntax  
  
```  
  
      inline int CommonPrefix(  
   const char* pszFile1,  
   const char* pszFile2,  
   char* pszDest   
);  
inline int CommonPrefix(  
   const wchar_t* pszFile1,  
   const wchar_t* pszFile2,  
   wchar_t* pszDest   
);  
```  
  
## Remarks  
 See [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574)