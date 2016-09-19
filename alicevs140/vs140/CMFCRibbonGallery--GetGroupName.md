---
title: "CMFCRibbonGallery::GetGroupName"
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
ms.assetid: 186c60de-19bc-4206-bab8-817a05773e08
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::GetGroupName
Returns the name of the group that is located at the specified index.  
  
## Syntax  
  
```  
LPCTSTR GetGroupName(  
    int nGroupIndex   
) const;  
```  
  
#### Parameters  
 [in] `nGroupIndex`  
 Specifies the zero-based index for the group whose name you want to retrieve.  
  
## Return Value  
 The name of the group located at the specified index. Passing an invalid index will result in a failed assertion.  
  
## Remarks  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)