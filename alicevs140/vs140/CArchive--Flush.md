---
title: "CArchive::Flush"
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
ms.assetid: d0d2eaf7-d504-42a8-8c25-d22e729b49fd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::Flush
Forces any data remaining in the archive buffer to be written to the file.  
  
## Syntax  
  
```  
  
void Flush( );  
```  
  
## Remarks  
 The member function `Flush` ensures that all data is transferred from the archive to the file. You must call [CFile::Close](../vs140/CFile--Close.md) to complete the transfer from the file to the storage medium.  
  
## Example  
 [!CODE [NVC_MFCSerialization#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#13)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::Close](../vs140/CArchive--Close.md)   
 [CFile::Flush](../vs140/CFile--Flush.md)   
 [CFile::Close](../vs140/CFile--Close.md)