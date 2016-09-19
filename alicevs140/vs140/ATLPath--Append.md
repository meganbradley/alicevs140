---
title: "ATLPath::Append"
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
ms.assetid: 73b5543a-224b-44f1-aa98-eb84e464833c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::Append
This function is an overloaded wrapper for [PathAppend](http://msdn.microsoft.com/library/windows/desktop/bb773565).  
  
## Syntax  
  
```  
  
      inline BOOL Append(  
   char* pszPath,  
   const char* pszMore   
);  
inline BOOL Append(  
   wchar_t* pszPath,  
   const wchar_t* pszMore   
);  
```  
  
## Remarks  
 See [PathAppend](http://msdn.microsoft.com/library/windows/desktop/bb773565) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathAppend](http://msdn.microsoft.com/library/windows/desktop/bb773565)