---
title: "CFile::SeekToBegin"
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
ms.assetid: b33a72da-2773-4b17-bf65-28670495167e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::SeekToBegin
Sets the value of the file pointer to the beginning of the file.  
  
## Syntax  
  
```  
  
void SeekToBegin( );  
```  
  
## Remarks  
 `SeekToBegin()` is equivalent to `Seek( 0L, CFile::begin )`.  
  
## Example  
 [!CODE [NVC_MFCFiles#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#19)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)