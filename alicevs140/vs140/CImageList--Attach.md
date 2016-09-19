---
title: "CImageList::Attach"
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
ms.assetid: 27486038-34a9-410b-885c-7b46616f037f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::Attach
Call this function to attach an image list to a `CImageList` object.  
  
## Syntax  
  
```  
  
      BOOL Attach(  
   HIMAGELIST hImageList   
);  
```  
  
#### Parameters  
 `hImageList`  
 A handle to an image list object.  
  
## Return Value  
 Nonzero if the attachment was successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#2)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::Detach](../vs140/CImageList--Detach.md)   
 [CImageList::GetSafeHandle](../vs140/CImageList--GetSafeHandle.md)