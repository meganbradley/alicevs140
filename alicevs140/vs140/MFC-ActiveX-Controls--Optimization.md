---
title: "MFC ActiveX Controls: Optimization"
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
ms.assetid: 8b11f26a-190d-469b-b594-5336094a0109
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Optimization
This article explains techniques you can use to optimize your ActiveX controls for better performance.  
  
 The topics [Turning Off the Activate When Visible Option](../vs140/Turning-off-the-Activate-When-Visible-Option.md) and [Providing Mouse Interaction While Inactive](../vs140/Providing-Mouse-Interaction-While-Inactive.md) discuss controls that don't create a window until activated. The topic [Providing Windowless Activation](../vs140/Providing-Windowless-Activation.md) discusses controls that never create a window, even when they are activated.  
  
 Windows have two major drawbacks for OLE objects: they prevent objects from being transparent or nonrectangular when active, and they add a large overhead to the instantiation and display of controls. Typically, creating a window takes 60 percent of a control's creation time. With a single shared window (usually the container's) and some dispatching code, a control receives the same window services, generally without a loss of performance. Having a window is mostly unnecessary overhead for the object.  
  
 Some optimizations do not necessarily improve performance when your control is used in certain containers. For example, containers released prior to 1996 did not support windowless activation, so implementing this feature will not provide a benefit in older containers. However, nearly every container supports persistence, so optimizing your control's persistence code will likely improve its performance in any container. If your control is specifically intended to be used with one particular type of container, you may want to research which of these optimizations is supported by that container. In general, however, you should try to implement as many of these techniques as are applicable to your particular control to ensure your control performs as well as it possibly can in a wide array of containers.  
  
 You can implement many of these optimizations through the [MFC ActiveX Control Wizard](../vs140/MFC-ActiveX-Control-Wizard.md), on the [Control Settings](../vs140/Control-Settings--MFC-ActiveX-Control-Wizard.md) page.  
  
### MFC ActiveX Control Wizard OLE Optimization Options  
  
|Control setting in the MFC ActiveX Control Wizard|Action|More information|  
|-------------------------------------------------------|------------|----------------------|  
|**Activate when visible** check box|Clear|[Turning Off the Activate When Visible Option](../vs140/Turning-off-the-Activate-When-Visible-Option.md)|  
|**Windowless activation** check box|Select|[Providing Windowless Activation](../vs140/Providing-Windowless-Activation.md)|  
|**Unclipped device context** check box|Select|[Using an Unclipped Device Context](../vs140/Using-an-Unclipped-Device-Context.md)|  
|**Flicker-free activation** check box|Select|[Providing Flicker-Free Activation](../vs140/Providing-Flicker-Free-Activation.md)|  
|**Mouse pointer notifications when inactive** check box|Select|[Providing Mouse Interaction While Inactive](../vs140/Providing-Mouse-Interaction-While-Inactive.md)|  
|**Optimized drawing code** check box|Select|[Optimizing Control Drawing](../vs140/Optimizing-Control-Drawing.md)|  
  
 For detailed information about the member functions that implement these optimizations, see [COleControl](../vs140/COleControl-Class.md). The member functions are listed by use, such as [Windowless Operations](assetId:///e9e28f79-9a70-4ae4-a5aa-b3e92f1904df) and [Inactive Pointer Handling Functions](assetId:///e9e28f79-9a70-4ae4-a5aa-b3e92f1904df).  
  
 For more information, see:  
  
-   [Optimizing Persistence and Initialization](../vs140/Optimizing-Persistence-and-Initialization.md)  
  
-   [Providing Windowless Activation](../vs140/Providing-Windowless-Activation.md)  
  
-   [Turning Off the Activate When Visible Option](../vs140/Turning-off-the-Activate-When-Visible-Option.md)  
  
-   [Providing Mouse Interaction While Inactive](../vs140/Providing-Mouse-Interaction-While-Inactive.md)  
  
-   [Providing Flicker-Free Activation](../vs140/Providing-Flicker-Free-Activation.md)  
  
-   [Using an Unclipped Device Context](../vs140/Using-an-Unclipped-Device-Context.md)  
  
-   [Optimizing Control Drawing](../vs140/Optimizing-Control-Drawing.md)  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)