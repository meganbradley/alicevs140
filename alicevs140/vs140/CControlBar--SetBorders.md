---
title: "CControlBar::SetBorders"
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
ms.assetid: ab381f6c-2dc6-46af-baf0-0ba408f73df1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::SetBorders
Call this function to set the size of the control bar's borders.  
  
## Syntax  
  
```  
  
      void SetBorders(  
   int cxLeft = 0,  
   int cyTop = 0,  
   int cxRight = 0,  
   int cyBottom = 0   
);  
void SetBorders(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 *cxLeft*  
 The width (in pixels) of the control bar's left border.  
  
 *cyTop*  
 The height (in pixels) of the control bar's top border.  
  
 *cxRight*  
 The width (in pixels) of the control bar's right border.  
  
 *cyBottom*  
 The height (in pixels) of the control bar's bottom border.  
  
 `lpRect`  
 A pointer to a [CRect](../vs140/CRect-Class.md) object that contains the current width (in pixels)of each border of the control bar object.  
  
## Example  
 The following code example sets the top and bottom borders of the control bar to 5 pixels, and the left and right borders to 2 pixels:  
  
 [!CODE [NVC_MFCControlLadenDialog#61](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#61)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CControlBar::GetBorders](../vs140/CControlBar--GetBorders.md)