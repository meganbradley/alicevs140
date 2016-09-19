---
title: "CFile::SeekToEnd"
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
ms.assetid: 7c53dac3-e0db-4112-a3da-f332cb74388d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::SeekToEnd
Sets the value of the file pointer to the logical end of the file.  
  
## Syntax  
  
```  
  
ULONGLONG SeekToEnd( );  
```  
  
## Return Value  
 The length of the file in bytes.  
  
## Remarks  
 `SeekToEnd()` is equivalent to `CFile::Seek( 0L, CFile::end )`.  
  
## Example  
 [!CODE [NVC_MFCFiles#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#19)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::GetLength](../vs140/CFile--GetLength.md)   
 [CFile::Seek](../vs140/CFile--Seek.md)   
 [CFile::SeekToBegin](../vs140/CFile--SeekToBegin.md)