---
title: "Properties Window Fields and Interfaces"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0328f0e5-2380-4a7a-a872-b547cb775050
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Properties Window Fields and Interfaces
The model for selection to determine what information is displayed in the **Properties** window is based on the window that has focus in the IDE. Every window, and object within the selected window, can have its selection context object pushed to the global selection context. The environment updates the global selection context with values from a window frame when that window has the focus. When the focus changes, so does the selection context.  
  
## Tracking Selection in the IDE  
 The window frame or site, owned by the IDE, has a service called <xref:Microsoft.VisualStudio.Shell.Interop.STrackSelection?qualifyHint=False>. The following steps show how a change in a selection, caused by the user either changing focus to another open window or selecting a different project item in **Solution Explorer**, is implemented to change the content displayed in the **Properties** window.  
  
1.  The object created by your VSPackage that is sited in the selected window calls <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider.QueryService?qualifyHint=False> to have <xref:Microsoft.VisualStudio.Shell.Interop.STrackSelection?qualifyHint=False> invoke <xref:Microsoft.VisualStudio.Shell.Interop.ITrackSelection?qualifyHint=False>.  
  
2.  The selection container, provided by the selected window, creates its own <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer?qualifyHint=False> object. When the selection changes, the VSPackage calls <xref:Microsoft.VisualStudio.Shell.Interop.ITrackSelection.OnSelectChange?qualifyHint=False> to notify any listeners in the environment, including the **Properties** window, of the change. It also provides access to hierarchy and item information related to the new selection.  
  
3.  Calling <xref:Microsoft.VisualStudio.Shell.Interop.ITrackSelection.OnSelectChange?qualifyHint=False> and passing it the selected hierarchy items in the `VSHPROPID_BrowseObject` parameter populates the <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer?qualifyHint=False> object.  
  
4.  An object derived from the [IDispatch Interface](assetId:///ebbff4bc-36b2-4861-9efa-ffa45e013eb5) is returned for <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_BrowseObject?qualifyHint=False> for the item requested, and the environment wraps it into an <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer?qualifyHint=False> (see the following step). If the call fails, the environment makes a second call to `IVsHierarchy::GetProperty`, passing it the selection container <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_SelContainer?qualifyHint=False> that the hierarchy item or items supply.  
  
     Your project VSPackage does not create <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer?qualifyHint=False> because the environment-supplied window VSPackage that implements it (for example, **Solution Explorer**) constructs <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer?qualifyHint=False> on its behalf.  
  
5.  The environment invokes the methods of <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer?qualifyHint=False> to get the objects based on the `IDispatch` interface to fill in the **Properties** window.  
  
 When a value in the **Properties** window is changed, VSPackages implement `IVsTrackSelectionEx::OnElementValueChangeEx` and `IVsTrackSelectionEx::OnSelectionChangeEx` to report the change to the element value. The environment then invokes <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell?qualifyHint=False> or <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer?qualifyHint=False> to keep the information displayed in the **Properties** window synchronized with the property values. For more information, see [How to: Update Property Values in the Properties Window](../vs140/Updating-Property-Values-in-the-Properties-Window.md).  
  
 In addition to selecting a different project item in **Solution Explorer** to display properties related to that item, you can also choose a different object from within a form or document window using the drop-down list available on the **Properties** window. For more information, see [Properties Window Object List](../Topic/Properties%20Window%20Object%20List.md).  
  
 You can change the way information is displayed in the **Properties** window grid from alphabetical to categorical, and, if available, you can also open a property page for a selected object by clicking the appropriate buttons on the **Properties** window. For more information, see [Properties Window Buttons](../vs140/Properties-Window-Buttons.md) and [Property Pages](../Topic/Property%20Pages.md).  
  
 Finally, the bottom of the **Properties** window also contains a description of the field selected in the **Properties** window grid. For more information, see [Getting Field Descriptions from the Properties Window](../vs140/Getting-Field-Descriptions-from-the-Properties-Window.md).  
  
## See Also  
 [Extending Properties](../Topic/Extending%20Properties.md)