---
title: "Playing Sounds (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f0d9e4ab-57c7-47b6-86d3-99ff07078040
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Playing Sounds (Visual Basic)
The `My.Computer.Audio` object provides methods for playing sounds.  
  
## Playing Sounds  
 Background playing lets the application execute other code while the sound plays. The `My.Computer.Audio.Play` method allows the application to play only one background sound at a time; when the application plays a new background sound, it stops playing the previous background sound. You can also play a sound and wait for it to complete.  
  
 In the following example, the `My.Computer.Audio.Play` method plays a sound. When `AudioPlayMode.WaitToComplete` is specified, `My.Computer.Audio.Play` waits until the sound completes before calling code continues. When using this example, you should ensure that the file name refers to a .wav sound file that is on your computer  
  
 [!CODE [VbVbalrMyComputer#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#15)]  
  
 In the following example, the `My.Computer.Audio.Play` method plays a sound. When using this example, you should ensure that the application resources include a .wav sound file that is named Waterfall.  
  
 [!CODE [VbVbalrMyComputer#16](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#16)]  
  
## Playing Looping Sounds  
 In the following example, the `My.Computer.Audio.Play` method plays the specified sound in the background when `PlayMode.BackgroundLoop` is specified. When using this example, you should ensure that the file name refers to a .wav sound file that is on your computer.  
  
 [!CODE [VbVbalrMyComputer#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#11)]  
  
 In the following example, the `My.Computer.Audio.Play` method plays the specified sound in the background when `PlayMode.BackgroundLoop` is specified. When using this example, you should ensure that the application resources include a .wav sound file that is named Waterfall.  
  
 [!CODE [VbVbalrMyComputer#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#12)]  
  
 The preceding code example is also available as an IntelliSense code snippet. In the code snippet picker, it is located in **Windows Forms Applications > Sound**. For more information, see [Code Snippets](../vs140/Code-Snippets.md).  
  
 In general, when an application plays a looping sound, it should eventually stop the sound.  
  
## Stopping the Playing of Sounds in the Background  
 Use the `My.Computer.Audio.Stop` method to stop the application's currently playing background or looping sound.  
  
 In general, when an application plays a looping sound, it should stop the sound at some point.  
  
 The following example stops a sound that is playing in the background.  
  
 [!CODE [VbVbalrMyComputer#18](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#18)]  
  
 The preceding code example is also available as an IntelliSense code snippet. In the code snippet picker, it is located in **Windows Forms Applications > Sound**. For more information, see [Code Snippets](../vs140/Code-Snippets.md).  
  
## Playing System Sounds  
 Use the `My.Computer.Audio.PlaySystemSound` method to play the specified system sound.  
  
 The `My.Computer.Audio.PlaySystemSound` method takes as a parameter one of the shared members from the <xref:System.Media.SystemSound?qualifyHint=False> class. The system sound <xref:System.Media.SystemSounds.Asterisk?qualifyHint=False> generally denotes errors.  
  
 The following example uses the `My.Computer.Audio.PlaySystemSound` method to play a system sound.  
  
 [!CODE [VbVbalrMyComputer#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#17)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.Devices.Audio?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Devices.Audio.Play?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Devices.Audio.PlaySystemSound?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Devices.Audio.Stop?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.AudioPlayMode?qualifyHint=False>