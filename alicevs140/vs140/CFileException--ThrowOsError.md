---
title: "CFileException::ThrowOsError"
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
ms.assetid: d0ef7b4a-bb07-4213-9c62-e9a6ceb6535e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileException::ThrowOsError
Throws a `CFileException` corresponding to a given `lOsError` value. If the error code is unknown, then the function throws an exception coded as **CFileException::generic**.  
  
## Syntax  
  
```  
  
      static void PASCAL ThrowOsError(  
   LONG lOsError,  
   LPCTSTR lpszFileName = NULL   
);  
```  
  
#### Parameters  
 `lOsError`  
 An operating-system-specific error code.  
  
 `lpszFileName`  
 A pointer to the string containing the name of the file that caused the exception, if available.  
  
## Example  
 [!CODE [NVC_MFCFiles#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#29)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileException Class](../vs140/CFileException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileException::ThrowErrno](../vs140/CFileException--ThrowErrno.md)