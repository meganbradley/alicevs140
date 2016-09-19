---
title: "CImageList::ExtractIcon"
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
ms.assetid: 7ec50e7e-9a7e-46b2-b072-7139b7129a24
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::ExtractIcon
Call this function to create an icon based on an image and its related mask in an image list.  
  
## Syntax  
  
```  
  
      HICON ExtractIcon(  
   int nImage   
);  
```  
  
#### Parameters  
 `nImage`  
 Zero-based index of the image.  
  
## Return Value  
 Handle of the icon if successful; otherwise **NULL**.  
  
## Remarks  
 This method relies on the behavior of the [ImageList_ExtractIcon](http://msdn.microsoft.com/library/windows/desktop/bb761401) macro to create the icon. Refer to the [ImageList_ExtractIcon](http://msdn.microsoft.com/library/windows/desktop/bb761401) macro for more information on icon creation and cleanup.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#12)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::Replace](../vs140/CImageList--Replace.md)