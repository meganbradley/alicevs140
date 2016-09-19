---
title: "CImageList::FromHandlePermanent"
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
ms.assetid: a1bef964-a759-49a1-b27d-f4bc697a30d2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::FromHandlePermanent
Returns a pointer to a `CImageList` object when given a handle to an image list.  
  
## Syntax  
  
```  
  
      static CImageList* PASCAL FromHandlePermanent(  
   HIMAGELIST hImageList   
);  
```  
  
#### Parameters  
 `hImageList`  
 Specifies the image list.  
  
## Return Value  
 A pointer to a `CImageList` object if successful; otherwise **NULL**.  
  
## Remarks  
 If a `CImageList` object is not attached to the handle, **NULL** is returned.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#14)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::FromHandle](../vs140/CImageList--FromHandle.md)