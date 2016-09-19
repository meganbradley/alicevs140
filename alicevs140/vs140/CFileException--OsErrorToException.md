---
title: "CFileException::OsErrorToException"
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
ms.assetid: f7358537-a61e-47ef-a967-7e21f609710f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileException::OsErrorToException
Returns an enumerator that corresponds to a given `lOsError` value. If the error code is unknown, then the function returns **CFileException::generic**.  
  
## Syntax  
  
```  
  
      static int PASCAL OsErrorToException(  
   LONG lOsError   
);  
```  
  
#### Parameters  
 `lOsError`  
 An operating-system-specific error code.  
  
## Return Value  
 Enumerated value that corresponds to a given operating-system error value.  
  
## Example  
 [!CODE [NVC_MFCFiles#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#27)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileException Class](../vs140/CFileException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileException::ErrnoToException](../vs140/CFileException--ErrnoToException.md)