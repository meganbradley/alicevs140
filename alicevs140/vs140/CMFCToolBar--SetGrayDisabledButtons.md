---
title: "CMFCToolBar::SetGrayDisabledButtons"
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
ms.assetid: c3020080-d916-4979-a2a0-24a5519ef3e3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetGrayDisabledButtons
Specifies whether unavailable buttons on the toolbar are dimmed, or whether button-unavailable images are used.  
  
## Syntax  
  
```  
void SetGrayDisabledButtons(  
   BOOL bGrayDisabledButtons   
);  
```  
  
#### Parameters  
 [in] `bGrayDisabledButtons`  
 A Boolean value that specifies how to display unavailable buttons. If this parameter is `TRUE`, the framework dims the buttons. Otherwise, the framework uses the collection of button-unavailable images.  
  
## Remarks  
 By default, unavailable buttons are dimmed.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)