---
title: "Using Tooltips in a CStatusBarCtrl Object"
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
ms.assetid: a77597a7-43ef-4b8f-87bc-a8ea1dc63dc3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Tooltips in a CStatusBarCtrl Object
To enable tooltips for a status bar control, create the `CStatusBarCtrl` object with the **SBT_TOOLTIPS** style.  
  
> [!NOTE]
>  If you are using a `CStatusBar` object to implement your status bar, use the `CStatusBar::CreateEx` function. It allows you to specify additional styles for the embedded **CStatusBarCtrl** object.  
  
 Once the `CStatusBarCtrl` object has been successfully created, use [CStatusBarCtrl::SetTipText](../vs140/CStatusBarCtrl--SetTipText.md) and [CStatusBarCtrl::GetTipText](../vs140/CStatusBarCtrl--GetTipText.md) to set and retrieve the tip text for a specific pane.  
  
 Once the tool tip has been set, it is displayed only if the part has an icon and no text, or if all of the text cannot be displayed inside the part. Tool tips are not supported in simple mode.  
  
## See Also  
 [Using CStatusBarCtrl](../vs140/Using-CStatusBarCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)