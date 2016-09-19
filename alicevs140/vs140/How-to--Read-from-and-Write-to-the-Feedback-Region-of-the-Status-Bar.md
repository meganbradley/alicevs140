---
title: "How to: Read from and Write to the Feedback Region of the Status Bar"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e639561c-e1e7-4660-b2a2-8bca80f34a29
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Read from and Write to the Feedback Region of the Status Bar
The Feedback region of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] status bar displays text. You can set and retrieve text, display static text, and highlight the displayed text.  
  
### To use the Feedback region of the Visual Studio Status bar  
  
1.  Obtain an instance of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar?qualifyHint=False> interface, which is made available through the <xref:Microsoft.VisualStudio.Shell.Interop.SVsStatusbar?qualifyHint=False> service.  
  
2.  Determine whether the status bar is frozen by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.IsFrozen?qualifyHint=False> method of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar?qualifyHint=False> instance.  
  
3.  Set the text of the Feedback region by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.SetText?qualifyHint=False> method and passing in a text string.  
  
4.  Read the text of the Feedback region by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.GetText?qualifyHint=False> method.  
  
## Example  
 This example demonstrates how to write text to and read text from the Feedback region.  
  
 [!CODE [VSSDKFeedbackStatusBar#1](../CodeSnippet/VS_Snippets_VSSDK/vssdkfeedbackstatusbar#1)]  
  
 In the above example, the code does the following things:  
  
-   Obtains an instance of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar?qualifyHint=False> interface from the <xref:Microsoft.VisualStudio.Shell.Interop.SVsStatusbar?qualifyHint=False> service.  
  
-   Checks to see if the status bar is frozen by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.IsFrozen?qualifyHint=False> method.  
  
-   Inhibits further updates to the status bar by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.FreezeOutput?qualifyHint=False> method.  
  
-   Reads the text from the status bar by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.GetText?qualifyHint=False> method and displays it in a message box.  
  
-   Allows updates to the status bar by calling <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.FreezeOutput?qualifyHint=False> and passing 0 in the parameter.  
  
-   Clears the contents of the status bar by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.Clear?qualifyHint=False> method.  
  
## See Also  
 [Status Bar Overview](../vs140/Extending-the-Status-Bar.md)   
 [How to: Program the Progress Bar Region of the Status Bar](../vs140/How-to--Program-the-Progress-Bar-Region-of-the-Status-Bar.md)   
 [How to: Use the Animation Region of the Status Bar](../Topic/How%20to:%20Use%20the%20Animation%20Region%20of%20the%20Status%20Bar.md)   
 [How to: Program the Designer Region of the Status Bar](../vs140/How-to--Program-the-Designer-Region-of-the-Status-Bar.md)