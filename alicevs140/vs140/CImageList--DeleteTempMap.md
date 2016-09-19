---
title: "CImageList::DeleteTempMap"
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
ms.assetid: 36a3fe17-e8df-4e0b-9d7d-662eb4354c37
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::DeleteTempMap
Called automatically by the `CWinApp` idle-time handler, `DeleteTempMap` deletes any temporary `CImageList` objects created by [FromHandle](../vs140/CImageList--FromHandle.md), but does not destroy any handles (`hImageList`) temporarily associated with the **ImageList** objects.  
  
## Syntax  
  
```  
  
static void PASCAL DeleteTempMap( );  
  
```  
  
## Example  
 [!CODE [NVC_MFC_CImageList#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)