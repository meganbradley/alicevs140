---
title: "ATLPath::FileExists"
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
ms.assetid: 18c377d1-2393-45ee-bdac-7076634af5cb
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::FileExists
This function is an overloaded wrapper for [PathFileExists](http://msdn.microsoft.com/library/windows/desktop/bb773584).  
  
## Syntax  
  
```  
  
      inline BOOL FileExists(  
   const char* pszPath   
);  
inline BOOL FileExists(  
   const wchar_t* pszPath   
);  
```  
  
## Remarks  
 See [PathFileExists](http://msdn.microsoft.com/library/windows/desktop/bb773584) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathFileExists](http://msdn.microsoft.com/library/windows/desktop/bb773584)