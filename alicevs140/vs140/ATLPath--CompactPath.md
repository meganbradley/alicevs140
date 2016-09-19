---
title: "ATLPath::CompactPath"
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
ms.assetid: f384983e-900e-49d8-a908-13c208cd0a68
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::CompactPath
This function is an overloaded wrapper for [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575).  
  
## Syntax  
  
```  
  
      inline BOOL CompactPath(  
   HDC hDC,  
   char* pszPath,  
   UINT dx   
);  
inline BOOL CompactPath(  
   HDC hDC,  
   wchar_t* pszPath,  
   UINT dx   
);  
```  
  
## Remarks  
 See [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575)