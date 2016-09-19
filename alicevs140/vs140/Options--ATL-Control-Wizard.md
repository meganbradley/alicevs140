---
title: "Options, ATL Control Wizard"
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
ms.topic: reference
ms.assetid: 4607c51a-992d-433e-9281-919c6f519a3d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Options, ATL Control Wizard
Insert "Search Results" summary here.  
  
 Use this page of the wizard to define the type of control you are creating and the level of interface support it contains.  
  
## UIElement List  
 **Control type**  
 The kind of control you want to create.  
  
-   **Standard control: An ActiveX control.**  
  
-   **Composite control**: An ActiveX control that can contain (similar to a dialog box) other ActiveX controls or Windows controls. A composite control includes the following:  
  
    -   A template for the dialog box that implements the composite control.  
  
    -   A custom resource, REGISTRY, which automatically registers the composite control when invoked.  
  
    -   A C++ class that implements the composite control.  
  
    -   A COM interface, exposed by the composite control.  
  
    -   An HTML test page containing the composite control.  
  
     By default, this control sets [CComControlBase::m_bWindowOnly](../vs140/CComControlBase--m_bWindowOnly.md) to true, to indicate that this is a windowed control. It implements a sink map. For more information, see [ATL Support for DHTML Controls](../vs140/ATL-Support-for-DHTML-Controls.md).  
  
-   **DHTML control**: An ATL DHTML control specifies the user interface, using HTML. The DHTML UI class contains a COM map. By default, this control sets [CComControlBase::m_bWindowOnly](../vs140/CComControlBase--m_bWindowOnly.md) to true, to indicate that this is a windowed control.  
  
     For more information, see [Identifying the Elements of the DHTML Control Project](../vs140/Identifying-the-Elements-of-the-DHTML-Control-Project.md).  
  
 **Minimal control**  
 Supports only the interfaces that are absolutely needed by most containers. You can set **Minimal control** for any of the control types: you can create a minimal standard control, a minimal composite control, or a minimal DHTML control.  
  
 **Aggregation**  
 Adds aggregation support for the control you are creating. For more information, see [Aggregation](../vs140/Aggregation.md).  
  
-   **Yes**: Create a control that can be aggregated.  
  
-   **No**: Create a control that cannot be aggregated.  
  
-   **Only**: Create a control that can only be instantiated through aggregation.  
  
 **Threading model**  
 Specifies that the threading model used by the control.  
  
-   **Single**: The control will run only in the primary COM thread.  
  
-   **Apartment**: The control can be created in any single thread apartment. The default.  
  
 **Interface**  
 The type of interface this control exposes to the container.  
  
-   **Dual**: Creates an interface that exposes properties and methods through `IDispatch` and directly through the VTBL.  
  
-   **Custom**: Creates an interface that exposes methods directly through a VTBL.  
  
     If you select **Custom**, then you can specify that the control is **Automation compatible**. If you select **Automation compatible**, then the wizard adds the [oleautomation](../vs140/oleautomation.md) attribute to the interface in the IDL, and the interface can be marshaled by the universal marshaler in oleaut32.dll. See [Marshaling Details](http://msdn.microsoft.com/library/windows/desktop/ms692621) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] for more information.  
  
     Additionally, if you select **Automation compatible**, then all parameters for all methods in the control must be **VARIANT** compatible.  
  
 **Support**  
 Sets additional miscellaneous support for the control.  
  
-   **Connection points**: Enables connection points for your object by making your object's class derive from [IConnectionPointContainerImpl](../vs140/IConnectionPointContainerImpl-Class.md) and allowing it to expose a source interface.  
  
-   **Licensed**: Adds support to the control for [licensing](http://msdn.microsoft.com/library/windows/desktop/ms690543). Licensed controls can only be hosted if the client machine has the correct license.  
  
## See Also  
 [ATL Control Wizard](../vs140/ATL-Control-Wizard.md)