---
title: "Setting the Mode of a CStatusBarCtrl Object"
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
ms.assetid: ca6076e5-1501-4e33-8d35-9308941e46c0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Setting the Mode of a CStatusBarCtrl Object
There are two modes for a `CStatusBarCtrl` object: simple and nonsimple. In the majority of cases, your status bar control will have one or more parts, along with text and perhaps an icon or icons. This is called the nonsimple mode. For more information on this mode, see [Initializing the Parts of a CStatusBarCtrl Object](../vs140/Initializing-the-Parts-of-a-CStatusBarCtrl-Object.md).  
  
 However, there are cases where you only need to display a single line of text. In this case, the simple mode is sufficient for your needs. To change the mode of the `CStatusBarCtrl` object to simple, make a call to the [SetSimple](../vs140/CStatusBarCtrl--SetSimple.md) member function. Once the status bar control is in simple mode, set the text by calling the **SetText** member function, passing 255 as the value for the **nPane** parameter.  
  
 You can use the [IsSimple](../vs140/CStatusBarCtrl--IsSimple.md) function to determine what mode the `CStatusBarCtrl` object is in.  
  
> [!NOTE]
>  If the status bar object is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn and, if applicable, any defined parts are automatically restored.  
  
## See Also  
 [Using CStatusBarCtrl](../vs140/Using-CStatusBarCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)