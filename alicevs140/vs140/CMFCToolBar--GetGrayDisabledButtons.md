---
title: "CMFCToolBar::GetGrayDisabledButtons"
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
ms.assetid: 67a0805c-7e25-4b29-8614-722da84e9df0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetGrayDisabledButtons
Specifies whether the images of disabled buttons are dimmed versions of the regular button images, or taken from the collection of disabled button images.  
  
## Syntax  
  
```  
BOOL GetGrayDisabledButtons() const;  
```  
  
## Return Value  
 `TRUE` to dim the images of disabled buttons; `FALSE`to obtain images from the collection of disabled images.  
  
## Remarks  
 Use [CMFCToolBar::SetGrayDisabledButtons](../vs140/CMFCToolBar--SetGrayDisabledButtons.md) to switch between dimmed images and the images from the collection of disabled images.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)