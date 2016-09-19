---
title: "CFile::GetLength"
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
ms.assetid: 63eb24ef-0e3a-4988-a93e-fe7726985967
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::GetLength
Obtains the current logical length of the file in bytes.  
  
## Syntax  
  
```  
  
virtual ULONGLONG GetLength( ) const;  
```  
  
## Return Value  
 The length of the file.  
  
## Example  
 [!CODE [NVC_MFCFiles#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#7)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::SetLength](../vs140/CFile--SetLength.md)