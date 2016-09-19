---
title: "CMFCToolBarImages::SetTransparentColor"
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
ms.assetid: 2892ddb1-eef9-48db-be53-a6409d742367
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::SetTransparentColor
Sets the transparent color of the toolbar images.  
  
## Syntax  
  
```  
COLORREF SetTransparentColor(  
   COLORREF clrTransparent   
);  
```  
  
#### Parameters  
 [in] `clrTransparent`  
 An RGB value.  
  
## Return Value  
 The previous transparent color.  
  
## Remarks  
 When you or the framework call [CMFCToolBarImages::Draw](../vs140/CMFCToolBarImages--Draw.md), the method does not draw any pixel that matches the color specified by `clrTransparent`.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)