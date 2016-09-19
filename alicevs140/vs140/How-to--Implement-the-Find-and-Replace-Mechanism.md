---
title: "How to: Implement the Find and Replace Mechanism"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bbd348db-3d19-42eb-99a2-3e808528c0ca
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# How to: Implement the Find and Replace Mechanism
Visual Studio provides two ways of implementing Find/Replace. One way is to pass a text image to the shell and let it handle searching, highlighting, and replacing text. This allows users to specify multiple text spans. Alternatively, your VSPackage can control this functionality itself. In both cases you must notify the shell about the current target and the targets for all open documents.  
  
### To implement Find/Replace  
  
1.  Implement the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget?qualifyHint=False> interface on one of the objects returned by the frame properties <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_DocView?qualifyHint=False> or <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_DocData?qualifyHint=False>. If you are creating a custom editor, you should implement this interface as part of the custom editor class.  
  
2.  Use the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetCapabilities?qualifyHint=False> method to specify the options that your editor supports and to indicate whether it implements text image searching.  
  
     If your editor supports text image searching, implement <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage?qualifyHint=False>.  
  
     Otherwise, implement <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find?qualifyHint=False> and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace?qualifyHint=False>.  
  
3.  If you implement the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find?qualifyHint=False> and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace?qualifyHint=False> methods, you can simplify your searching tasks by calling the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper?qualifyHint=False> interface.  
  
## See Also  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.__VSPROPID?qualifyHint=False>