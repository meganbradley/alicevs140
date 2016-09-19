---
title: "CFile::Remove"
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
ms.assetid: 819294a3-be29-47e2-b32c-e5ebf6e6e885
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Remove
This static function deletes the file specified by the path.  
  
## Syntax  
  
```  
  
      static void PASCAL Remove(  
   LPCTSTR lpszFileName,  
   CAtlTransactionManager* pTM = NULL  
);  
```  
  
#### Parameters  
 `lpszFileName`  
 A string that is the path to the desired file. The path can be relative or absolute, and can contain a network name.  
  
 `pTM`  
 Pointer to CAtlTransactionManager object  
  
## Remarks  
 It will not remove a directory.  
  
 The **Remove** member function throws an exception if the connected file is open or if the file cannot be removed. This is equivalent to the DEL command.  
  
## Example  
 [!CODE [NVC_MFCFiles#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#17)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)