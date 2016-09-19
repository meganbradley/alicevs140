---
title: "ATLPath::RenameExtension"
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
ms.assetid: bc6f1e98-e247-4ecf-9e28-f5c2c51b2e93
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLPath::RenameExtension
This function is an overloaded wrapper for [PathRenameExtension](http://msdn.microsoft.com/library/windows/desktop/bb773749).  
  
## Syntax  
  
```  
  
      inline BOOL RenameExtension(  
   char* pszPath,  
   const char* pszExt   
);  
inline BOOL RenameExtension(  
   wchar_t* pszPath,  
   const wchar_t* pszExt   
);  
```  
  
## Remarks  
 See [PathRenameExtension](http://msdn.microsoft.com/library/windows/desktop/bb773749) for details.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [PathRenameExtension](http://msdn.microsoft.com/library/windows/desktop/bb773749)