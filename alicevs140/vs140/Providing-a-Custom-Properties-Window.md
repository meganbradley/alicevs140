---
title: "Providing a Custom Properties Window"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 408dcdef-8ef9-4644-97d2-f311cd35824f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Providing a Custom Properties Window
It is possible to provide your own **Properties** window for a given project system, instead of extending the **Properties** window provided by the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE). The most-often encountered scenario is when you yourself implement the object sited in the window frame.  
  
 In the event you do not implement the object sited in the window frame, but do still have access to it by some other means, there are a number of ways to access the <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame?qualifyHint=False> interface as listed in the last procedure on this page.  
  
### To provide your Properties window  
  
1.  Define a GUID that represents your **Properties** window implementation.  
  
2.  In your <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite?qualifyHint=False> implementation, use the <xref:Microsoft.VisualStudio.Shell.Interop.IProfferService?qualifyHint=False> service to proffer your **Properties** window as a service to the Visual Studio Environment.  
  
### To call your properties window  
  
1.  Call the <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane.SetSite?qualifyHint=False> method.  
  
2.  `QueryService` for <xref:Microsoft.VisualStudio.Shell.Interop.SVsTrackSelectionEx?qualifyHint=False> from the <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider?qualifyHint=False> passed into the <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane.SetSite?qualifyHint=False> method.  
  
3.  Obtain <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackSelectionEx?qualifyHint=False> from <xref:Microsoft.VisualStudio.Shell.Interop.SVsTrackSelectionEx?qualifyHint=False> service.  
  
4.  Call <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackSelectionEx.OnElementValueChange?qualifyHint=False> with first parameter set to `SEID_PropertyBrowserSID` (taken from the <xref:Microsoft.VisualStudio.VSConstants.VSSELELEMID?qualifyHint=False> enumeration), and the third parameter, `varValue`, representing a string form of the GUID that represents your **Properties** window. Make this call only once at the first creation of your **Properties** window document window. After the call this **Properties** window is associated with your window frame.  
  
### To obtain the Window Frame object when you are not the implementer  
  
-   You can `QueryService` for <xref:Microsoft.VisualStudio.Shell.Interop.SVsTrackSelectionEx?qualifyHint=False> service from <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.GetProperty?qualifyHint=False> with the parameter `propid` set to <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_SPFrame?qualifyHint=False>.  
  
-   You can obtain the active document window by calling <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.GetCurrentSelection?qualifyHint=False> through SVsMonitorSelection service. Set the parameter `elementid` to `SEID_WindowFrame`, taken from the <xref:Microsoft.VisualStudio.VSConstants.VSSELELEMID?qualifyHint=False> enumeration.  
  
## See Also  
 [Properties Window and Property Pages](../Topic/Extending%20Properties.md)   
 [Properties Window Fields and Interfaces](../vs140/Properties-Window-Fields-and-Interfaces.md)