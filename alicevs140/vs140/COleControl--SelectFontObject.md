---
title: "COleControl::SelectFontObject"
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
ms.assetid: 6efb627a-b791-4a09-9056-1c9cc98533cd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SelectFontObject
Selects a font into a device context.  
  
## Syntax  
  
```  
  
      CFont* SelectFontObject(  
   CDC* pDC,  
   CFontHolder& fontHolder   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to a device context object.  
  
 `fontHolder`  
 Reference to the [CFontHolder](../vs140/CFontHolder-Class.md) object representing the font to be selected.  
  
## Return Value  
 A pointer to the previously selected font. When the caller has finished all drawing operations that use *fontHolder,* it should reselect the previously selected font by passing it as a parameter to [CDC::SelectObject](../vs140/CDC--SelectObject.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)