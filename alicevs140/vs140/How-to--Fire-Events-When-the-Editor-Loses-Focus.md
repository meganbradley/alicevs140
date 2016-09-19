---
title: "How to: Fire Events When the Editor Loses Focus"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64d40695-6917-468a-8037-a253453ac159
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# How to: Fire Events When the Editor Loses Focus
Sometimes it is necessary to know when an editor loses focus on the window frame. For example, you might need to extract code from a code window after the editor is no longer focused on it. The following procedure provides the steps to follow to receive notification of the editor losing focus.  
  
### To fire an event in response to an editor losing focus  
  
1.  Monitor selection events by obtaining an <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection?qualifyHint=False> object from <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection?qualifyHint=False>.  
  
2.  Call <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.AdviseSelectionEvents?qualifyHint=False> and provide it your <xref:Microsoft.VisualStudio.Shell.Interop.IVsSelectionEvents?qualifyHint=False> object.  
  
3.  In your call to <xref:Microsoft.VisualStudio.Shell.Interop.IVsSelectionEvents.OnElementValueChanged?qualifyHint=False>, look for `elementid==SEID_WindowFrame`.  
  
4.  Test the `varValueNew` parameter for two things:  
  
    1.  The window frame you are looking for.  
  
    2.  The point at which your program loses the selection to that window frame.