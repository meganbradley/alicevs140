---
title: "CImageList::Write"
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
ms.assetid: 178bcb68-103d-4232-898e-568378fb88be
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::Write
Call this function to write an image list object to an archive.  
  
## Syntax  
  
```  
  
      BOOL Write(  
   CArchive* pArchive   
);  
```  
  
#### Parameters  
 `pArchive`  
 A pointer to a `CArchive` object in which the image list is to be stored.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#17)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::Read](../vs140/CImageList--Read.md)