---
title: "CMFCOutlookBar::SetButtonsFont"
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
ms.assetid: 86e0a492-e959-40cf-826f-abc054a93a3c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::SetButtonsFont
Sets the font of the text on the buttons of the Outlook bar.  
  
## Syntax  
  
```  
void SetButtonsFont(  
   CFont* pFont,  
   BOOL bRedraw=TRUE   
);  
```  
  
#### Parameters  
 [in] `pFont`  
 Specifies the new font.  
  
 [in] `bRedraw`  
 If `TRUE`, the Outlook bar will be redrawn.  
  
## Remarks  
 Use this method to set a font for the text displayed on outlook tab page buttons.  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)