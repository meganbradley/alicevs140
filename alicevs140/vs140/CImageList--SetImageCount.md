---
title: "CImageList::SetImageCount"
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
ms.assetid: 8ce75a9e-d8b8-40d3-991c-de26d78a218d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::SetImageCount
Call this member function to reset the number of images in a `CImageList` object.  
  
## Syntax  
  
```  
  
      BOOL SetImageCount(  
   UINT uNewCount   
);  
```  
  
#### Parameters  
 *uNewCount*  
 The value specifying the new total number of images in the image list.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 If you call this member function to increase the number of images in the image list, then call [Replace](../vs140/CImageList--Replace.md) for each additional image to assign the new indexes to valid images. If you fail to assign the indexes to valid images, draw operations that create the new images will be unpredictable.  
  
 If you decrease the size of an image list by using this function, the truncated images are freed.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#21)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)