---
title: "CMFCMenuBar::GetMenuFont"
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
ms.assetid: bcdadbc3-3fd4-4129-8a68-34777bcf33ae
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::GetMenuFont
Retrieves the current menu font.  
  
## Syntax  
  
```  
static const CFont& GetMenuFont(  
   BOOL bHorz = TRUE  
);  
```  
  
#### Parameters  
 [in] `bHorz`  
 A Boolean parameter that specifies whether to return the horizontal or vertical font. `TRUE` indicates the horizontal font.  
  
## Return Value  
 A pointer to a [CFont](../vs140/CFont-Class.md) parameter that contains the current menu bar font.  
  
## Remarks  
 The returned font is a global parameter for the application. Two global fonts are maintained for all `CMFCMenuBar` objects. These separate fonts are used for horizontal and vertical menu bars.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::SetMenuFont](../vs140/CMFCMenuBar--SetMenuFont.md)