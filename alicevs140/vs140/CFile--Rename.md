---
title: "CFile::Rename"
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
ms.assetid: b65539c5-ba0d-4a29-bfcf-c4d3beab2c09
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Rename
This static function renames the specified file.  
  
## Syntax  
  
```  
  
      static void PASCAL Rename(  
   LPCTSTR lpszOldName,  
   LPCTSTR lpszNewName,  
   CAtlTransactionManager* pTM = NULL  
);  
```  
  
#### Parameters  
 `lpszOldName`  
 The old path.  
  
 `lpszNewName`  
 The new path.  
  
 `pTM`  
 Pointer to CAtlTransactionManager object  
  
## Remarks  
 Directories cannot be renamed. This is equivalent to the REN command.  
  
## Example  
 [!CODE [NVC_MFCFiles#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#18)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)