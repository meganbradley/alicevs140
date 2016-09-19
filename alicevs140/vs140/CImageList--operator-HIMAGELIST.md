---
title: "CImageList::operator HIMAGELIST"
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
ms.assetid: 93591f0f-d97c-44e8-9278-7f083ac39e03
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::operator HIMAGELIST
Use this operator to get the attached handle of the `CImageList` object.  
  
## Syntax  
  
```  
  
operator HIMAGELIST( ) const;  
  
```  
  
## Return Value  
 If successful, a handle to the image list represented by the `CImageList` object; otherwise **NULL**.  
  
## Remarks  
 This operator is a casting operator, which supports direct use of an `HIMAGELIST` object.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#16)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)