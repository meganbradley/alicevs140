---
title: "Settings for the Tool Tip Control"
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
ms.topic: article
ms.assetid: ff8c5c46-2047-403a-bd98-ffec3d21ee3a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Settings for the Tool Tip Control
You can set the tool tip control ([CToolTipCtrl](../vs140/CToolTipCtrl-Class.md)) to be either active or inactive. When you set it to be active, the tool tip control appears when the cursor is on a tool. When you set it to be inactive, the tool tip control does not appear, even if the cursor is on a tool. Call [Activate](../vs140/CToolTipCtrl--Activate.md) to activate or deactivate a tool tip control.  
  
 You can set an active tool tip to display the tool tip when the cursor is on a tool, whether or not the tool tip control's owner window is active or inactive, by using the **TTS_ALWAYSTIP** style. If you do not use this style, the tool tip control appears when the tool's owner window is active, but not when it is inactive.  
  
 Most applications contain toolbars with tools that correspond to menu commands. For such tools, it is convenient for the tool tip control to display the same text as the corresponding menu item. The system automatically strips the ampersand (&) accelerator characters from all strings passed to a tool tip control, unless the control has the **TTS_NOPREFIX** style.  
  
## See Also  
 [Using CToolTipCtrl](../vs140/Using-CToolTipCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)