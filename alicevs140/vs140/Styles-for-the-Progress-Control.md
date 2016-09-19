---
title: "Styles for the Progress Control"
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
ms.assetid: 39eb8081-bc20-4552-91b9-e7cdd1b7d8ae
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Styles for the Progress Control
When you initially create the progress control ([CProgressCtrl::Create](../vs140/CProgressCtrl--Create.md)), use the `dwStyle` parameter to specify the desired window styles for your progress control. The following list details the applicable window styles. The control ignores any window style other than the ones listed here. You should always create the control as a child window, usually of a dialog box parent.  
  
|Window style|Effect|  
|------------------|------------|  
|`WS_BORDER`|Creates a border around the window.|  
|**WS_CHILD**|Creates a child window (should always be used for `CProgressCtrl`).|  
|**WS_CLIPCHILDREN**|Excludes the area occupied by child windows when you draw within the parent window. Used when you create the parent window.|  
|**WS_CLIPSIBLINGS**|Clips child windows relative to each other.|  
|**WS_DISABLED**|Creates a window that is initially disabled.|  
|**WS_VISIBLE**|Creates a window that is initially visible.|  
|**WS_TABSTOP**|Specifies that the control can receive focus when the user presses the TAB key to move to it.|  
  
 In addition, you can specify two styles that apply only to the progress control, `PBS_VERTICAL` and `PBS_SMOOTH`.  
  
 Use `PBS_VERTICAL` to orient the control vertically, rather than horizontally. Use `PBS_SMOOTH` to fill the control completely, rather than displaying small delineated squares that fill the control incrementally.  
  
 Without `PBS_SMOOTH` style:  
  
 ![Standard progress bar style](../vs140/media/vc4RUW1.gif "vc4RUW1")  
  
 With `PBS_SMOOTH` and `PBS_VERTICAL` styles:  
  
 ![Progress bar style, smooth and vertical](../vs140/media/vc4RUW2.gif "vc4RUW2")  
  
 For more information, see [Window Styles](../vs140/Frame-Window-Styles--MFC-.md) in the *MFC Reference*.  
  
## See Also  
 [Using CProgressCtrl](../vs140/Using-CProgressCtrl.md)