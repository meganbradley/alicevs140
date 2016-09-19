---
title: "Using CAnimateCtrl"
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
ms.assetid: 696c0805-bef0-4e2e-a9e7-b37b9215b7f0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using CAnimateCtrl
An animation control, represented by the class [CAnimateCtrl](../vs140/CAnimateCtrl-Class.md), is a window that displays a clip in Audio Video Interleaved (AVI) format — the standard Windows video/audio format. An AVI clip is a series of bitmap frames, like a movie.  
  
 Since your thread continues executing while the AVI clip is displayed, one common use for an animation control is to indicate system activity during a lengthy operation. For example, the Windows Find dialog box displays a moving magnifying glass as the system searches for a file.  
  
 Animation controls can only play simple AVI clips, and they do not support sound. (For a complete list of limitations, see [CAnimateCtrl](../vs140/CAnimateCtrl-Class.md).) Since the capabilities of an animation control are severely limited and subject to change, you should use an alternative such as the MCIWnd control if you need a control to provide multimedia playback and/or recording capabilities. For more information about the MCIWnd control, see the multimedia documentation.  
  
## What do you want to know more about?  
  
-   [Using an Animation Control](../vs140/Using-an-Animation-Control.md)  
  
-   [Notifications Sent by Animation Controls](../vs140/Notifications-Sent-by-Animation-Controls.md)  
  
## See Also  
 [Controls (MFC)](../vs140/Controls--MFC-.md)