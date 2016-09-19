---
title: "CPaneFrameWnd::SetCaptionButtons"
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
ms.assetid: ad5da983-edf3-4da3-b509-1a7695b81af6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::SetCaptionButtons
Sets caption buttons.  
  
## Syntax  
  
```  
virtual void SetCaptionButtons(  
   DWORD dwButtons  
);  
```  
  
#### Parameters  
 [in] `dwButtons`  
 Bitwise-OR combination of the following values:  
  
-   `AFX_CAPTION_BTN_CLOSE`  
  
-   `AFX_CAPTION_BTN_PIN`  
  
-   `AFX_CAPTION_BTN_MENU`  
  
-   `AFX_CAPTION_BTN_CUSTOMIZE`  
  
## Requirements  
 **Header:** afxpaneframewnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)