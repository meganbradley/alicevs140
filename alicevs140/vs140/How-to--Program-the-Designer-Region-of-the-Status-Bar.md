---
title: "How to: Program the Designer Region of the Status Bar"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 735a86bb-80b2-4557-9677-00799856017f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Program the Designer Region of the Status Bar
The Designer region of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] status bar displays information that pertains to editing, for example, the line number or column number of the cursor location.  
  
### To program the Designer region of the Visual Studio status bar  
  
1.  Obtain an instance of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar?qualifyHint=False> interface, which is made available through the <xref:Microsoft.VisualStudio.Shell.Interop.SVsStatusbar?qualifyHint=False> service.  
  
2.  Update the Designer region of the status bar by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.SetInsMode?qualifyHint=False> method and <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar.SetLineColChar?qualifyHint=False> method of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbar?qualifyHint=False> instance.  
  
## Example  
 This example demonstrates how to program the Designer region of the status bar.  
  
 [!CODE [VSSDKDesignerStatusBar#1](../CodeSnippet/VS_Snippets_VSSDK/vssdkdesignerstatusbar#1)]  
  
## See Also  
 [Status Bar](../vs140/Extending-the-Status-Bar.md)   
 [How to: Read from and Write to the Feedback Region of the Status Bar](../vs140/How-to--Read-from-and-Write-to-the-Feedback-Region-of-the-Status-Bar.md)   
 [How to: Program the Progress Bar Region of the Status Bar](../vs140/How-to--Program-the-Progress-Bar-Region-of-the-Status-Bar.md)   
 [How to: Use the Animation Region of the Status Bar](../Topic/How%20to:%20Use%20the%20Animation%20Region%20of%20the%20Status%20Bar.md)