---
title: "CArchive::GetFile"
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
ms.assetid: e2edf044-538b-4dfe-bc0e-7608d1dce179
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::GetFile
Gets the `CFile` object pointer for this archive.  
  
## Syntax  
  
```  
  
CFile* GetFile( ) const;  
```  
  
## Return Value  
 A constant pointer to the `CFile` object in use.  
  
## Remarks  
 You must flush the archive before using `GetFile`.  
  
## Example  
 [!CODE [NVC_MFCSerialization#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#14)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::Flush](../vs140/CArchive--Flush.md)