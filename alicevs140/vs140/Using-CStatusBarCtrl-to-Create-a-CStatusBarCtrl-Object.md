---
title: "Using CStatusBarCtrl to Create a CStatusBarCtrl Object"
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
ms.assetid: 365c2b65-12de-49e6-9a2e-416c6ee10d60
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using CStatusBarCtrl to Create a CStatusBarCtrl Object
Here is an example of a typical use of [CStatusBarCtrl](../vs140/CStatusBarCtrl-Class.md):  
  
### To use a status bar control with parts  
  
1.  Construct the `CStatusBarCtrl` object.  
  
2.  Call [SetMinHeight](../vs140/CStatusBarCtrl--SetMinHeight.md) if you want to set the minimum height of the status bar control's drawing area.  
  
3.  Call [SetBkColor](../vs140/CStatusBarCtrl--SetBkColor.md) to set the background color of the status bar control.  
  
4.  Call [SetParts](../vs140/CStatusBarCtrl--SetParts.md) to set the number of parts in a status bar control and the coordinate of the right edge of each part.  
  
5.  Call [SetText](../vs140/CStatusBarCtrl--SetText.md) to set the text in a given part of the status bar control. The message invalidates the portion of the control that has changed, causing it to display the new text when the control next receives the `WM_PAINT` message.  
  
 In some cases, the status bar only needs to display a line of text. In this case, make a call to [SetSimple](../vs140/CStatusBarCtrl--SetSimple.md). This puts the status bar control into "simple" mode, which displays a single line of text.  
  
## See Also  
 [Using CStatusBarCtrl](../vs140/Using-CStatusBarCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)