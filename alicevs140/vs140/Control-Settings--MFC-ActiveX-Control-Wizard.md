---
title: "Control Settings, MFC ActiveX Control Wizard"
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
ms.assetid: 2ccaa4fc-0d52-413e-afa3-ecd474c3f6f0
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control Settings, MFC ActiveX Control Wizard
Use this page of the wizard to specify how you want the control to behave. For example, you can base the control on standard Windows control types, optimize its behavior and appearance, or indicate that the control can act as a container for other controls.  
  
 For more information about how to select options on this page to maximize the efficiency of the control, see [MFC ActiveX Controls: Optimization](../vs140/MFC-ActiveX-Controls--Optimization.md).  
  
## UIElement List  
 **Create control based on**  
 On this list, you can select the kind of control from which your control should inherit. The list is a subset of the control classes that are available for `CreateWindowEx` and additional common controls that are specified in commctrl.h. Your selection determines the style of the control in the `PreCreateWindow` function in the *ProjName*Ctrl.cpp file. For more information, see [MFC ActiveX Controls: Subclassing a Windows Control](../vs140/MFC-ActiveX-Controls--Subclassing-a-Windows-Control.md).  
  
|Control|Description|  
|-------------|-----------------|  
|**BUTTON**|A Windows button control|  
|**COMBOBOX**|A Windows combo box control|  
|**EDIT**|A Windows edit box control|  
|**LISTBOX**|A Windows list box control|  
|**SCROLLBAR**|A Windows scroll bar control|  
|**STATIC**|A Windows static control|  
|**msctls_hotkey32**|A hot key common control|  
|**msctls_progress32**|A progress bar common control|  
|**msctls_statusbar32**|A status bar common control|  
|**msctls_trackbar32**|A track bar common control|  
|**msctls_updown32**|A spin button (or up-down) common control|  
|**SysAnimate32**|An animation common control|  
|**SysHeader32**|A header common control|  
|**SysListView32**|A list view common control|  
|**SysTabControl32**|A tab common control|  
|**SysTreeView32**|A tree view common control|  
  
 **Activates when visible**  
 Specifies that a window is created for the control when it is accessed. By default, the **Activates when visible** option is selected. If you want to defer control activation until the container requires it (for example, when a user clicks the mouse), clear this option. When this feature is off, the control does not incur the expense of window creation until it is required. For more information, see [Turning off the Activate When Visible Option](../vs140/Turning-off-the-Activate-When-Visible-Option.md).  
  
 **Invisible at run time**  
 Specifies that the control has no user interface at run time. A timer is a kind of control that you might want to be invisible.  
  
 **Has an About box dialog**  
 Specifies that the control has the standard Windows **About** dialog box, which displays version number and copyright information.  
  
> [!NOTE]
>  How the user accesses help for the control depends on how you have implemented the help and whether you have integrated the control help with the container help. For more information about how to integrate help, on the [MSDN Library](http://go.microsoft.com/fwlink/?linkID=150542) website, search for "Adding Context-Sensitive Help to an MFC ActiveX Control".  
  
 When you select this option, it inserts the `AboutBox` control method in the project control class (C*ProjName*Ctrl.cpp) and adds AboutBox to the project dispatch map. By default, this option is selected.  
  
 **Optimized drawing code**  
 Specifies that the container restores the original GDI objects automatically after all the container controls, which are drawn to the same device context, have been drawn. For more information about this feature, see [Optimizing Control Drawing](../vs140/Optimizing-Control-Drawing.md).  
  
 **Windowless activation**  
 Specifies that the control does not produce a window when it is activated. Windowless activation allows for nonrectangular or transparent controls, and a windowless control requires less system overhead than a control that has a window requires. A windowless control does not allow for an unclipped device context or flicker-free activation. Containers that were created before 1996 do not support windowless activation. For more information about how to use this option, see [Providing Windowless Activation](../vs140/Providing-Windowless-Activation.md).  
  
 **Unclipped device context**  
 Overrides [COleControl::GetControlFlags](../vs140/COleControl--GetControlFlags.md) in the control header (*projname*ctrl.h) to disable the call to `IntersectClipRect` made by `COleControl`. When you select this option, it provides a small speed advantage. If you select **Windowless activation**, this feature is not available. For more information, see [Using an Unclipped Device Context](../vs140/Using-an-Unclipped-Device-Context.md).  
  
 **Flicker-free activation**  
 Eliminates the drawing operations and the accompanying visual flicker that occur between the active and inactive states of the control. If you select **Windowless activation**, this feature is not available. When you set this option, the `noFlickerActivate` flag is one of the flags that are returned by [COleControl::GetControlFlags](../vs140/COleControl--GetControlFlags.md). For more information, see [Providing Flicker-Free Activation](../vs140/Providing-Flicker-Free-Activation.md).  
  
 **Available in Insert Object dialog**  
 Specifies that the control will be available in the **Insert Object** dialog box for enabled containers. When you select this option, the `afxRegInsertable` flag is one of the flags that are returned by `AfxOleRegisterControlClass`. By using the **Insert Object** dialog box, a user can insert newly created or existing objects into a compound document.  
  
 **Mouse pointer notifications when inactive**  
 Enables the control to process mouse pointer notifications, whether control is active or not. When you select this option, the `pointerInactive` flag is one of the flags that are returned by [COleControl::GetControlFlags](../vs140/COleControl--GetControlFlags.md). For more information about how to use this option, see [Providing Mouse Interaction While Inactive](../vs140/Providing-Mouse-Interaction-While-Inactive.md).  
  
 **Acts as a simple frame control**  
 Specifies that the control is a container for other controls by setting the `OLEMISC_SIMPLEFRAME` bit for the control. For more information, on the [MSDN Library](http://go.microsoft.com/fwlink/?linkID=150542) website, search for "Simple Frame Site Containment".  
  
 **Loads properties asynchronously**  
 Enables a reset of any previous asynchronous data and initiates a new load of the asynchronous property of the control.  
  
## See Also  
 [MFC ActiveX Control Wizard](../vs140/MFC-ActiveX-Control-Wizard.md)   
 [Application Settings, MFC ActiveX Control Wizard](../vs140/Application-Settings--MFC-ActiveX-Control-Wizard.md)   
 [Control Names, MFC ActiveX Control Wizard](../vs140/Control-Names--MFC-ActiveX-Control-Wizard.md)