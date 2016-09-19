---
title: "ATLPath::GetDriveNumber"
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
ms.assetid: 31f81f6f-c3cf-4f9f-9299-31d355b4631f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::GetDriveNumber
This function is an overloaded wrapper for [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612).  
  
## Syntax  
  
```  
  
      inline int GetDriveNumber(  
   const char* pszPath   
);  
inline int GetDriveNumber(  
   const wchar_t* pszPath   
);  
```  
  
## Remarks  
 See [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612)