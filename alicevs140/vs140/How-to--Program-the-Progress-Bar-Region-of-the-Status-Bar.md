---
title: "How to: Program the Progress Bar Region of the Status Bar"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b54616a-8c20-436d-b764-f2380e5760f2
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Program the Progress Bar Region of the Status Bar
The Progress Bar region of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] status bar displays the incremental progress of quick operations, for example, saving a file to disk.  
  
### To use the Progress Bar region of the Visual Studio status bar  
  
1.  Obtain an instance of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar?qualifyHint=False> interface, which is made available through the <xref:Microsoft.VisualStudio.Shell.Interop.SVsStatusbar?qualifyHint=False> service.  
  
2.  Initialize the progress bar to starting values by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.Progress?qualifyHint=False> method.  
  
3.  Update the progress bar as your operation proceeds by using the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.Progress?qualifyHint=False> method to set new values.  
  
## Example  
 This example demonstrates how to initialize and update the progress bar.  
  
 [!CODE [VSSDKProgressStatusBar#1](../CodeSnippet/VS_Snippets_VSSDK/vssdkprogressstatusbar#1)]  
  
 In the example, the code:  
  
-   Obtains an instance of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar?qualifyHint=False> interface from the <xref:Microsoft.VisualStudio.Shell.Interop.SVsStatusbar?qualifyHint=False> service.  
  
-   Initializes the progress bar to given starting values by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.Progress?qualifyHint=False> method.  
  
-   Simulates an operation by iterating through a `for` loop and updating the progress bar values by using the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.Progress?qualifyHint=False> method.  
  
-   Clears the progress bar by using the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.Clear?qualifyHint=False> method.  
  
## See Also  
 [Status Bar Overview](../vs140/Extending-the-Status-Bar.md)   
 [How to: Read from and Write to the Feedback Region of the Status Bar](../vs140/How-to--Read-from-and-Write-to-the-Feedback-Region-of-the-Status-Bar.md)   
 [How to: Use the Animation Region of the Status Bar](../Topic/How%20to:%20Use%20the%20Animation%20Region%20of%20the%20Status%20Bar.md)   
 [How to: Program the Designer Region of the Status Bar](../vs140/How-to--Program-the-Designer-Region-of-the-Status-Bar.md)