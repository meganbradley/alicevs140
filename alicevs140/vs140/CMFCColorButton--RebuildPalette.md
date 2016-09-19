---
title: "CMFCColorButton::RebuildPalette"
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
ms.assetid: eac5906d-91b8-44ce-b8a2-736457848fdc
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::RebuildPalette
Initializes the `m_pPalette` protected data member to the specified palette or the default system palette.  
  
## Syntax  
  
```  
void RebuildPalette(  
   CPalette* pPal  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pPal`|A pointer to a logical palette or `NULL`. If `NULL`, the default system palette is used.|  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPalette Class](../vs140/CPalette-Class.md)