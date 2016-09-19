---
title: "ActiveX Control Containers: Programming ActiveX Controls in an ActiveX Control Container"
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
ms.assetid: ef9b2480-92d6-4191-b16e-8055c4fd7b73
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ActiveX Control Containers: Programming ActiveX Controls in an ActiveX Control Container
This article describes the process for accessing the exposed [methods](../vs140/MFC-ActiveX-Controls--Methods.md) and [properties](../vs140/MFC-ActiveX-Controls--Properties.md) of embedded ActiveX controls. Basically, you will follow these steps:  
  
1.  [Insert an ActiveX control into the ActiveX container project](../vs140/ActiveX-Control-Containers--Inserting-a-Control-into-a-Control-Container-Application.md) using Gallery.  
  
2.  [Define a member variable](../vs140/ActiveX-Control-Containers--Connecting-an-ActiveX-Control-to-a-Member-Variable.md) (or other form of access) of the same type as the ActiveX control wrapper class.  
  
3.  [Program the ActiveX control](#_core_programming_the_activex_control) using predefined member functions of the wrapper class.  
  
 For this discussion, assume you've created a dialog-based project (named Container) with ActiveX control support. The Circ sample control, Circ, will be added to the resulting project.  
  
 Once the Circ control is inserted into the project (step 1), insert an instance of the Circ control into the application's main dialog box.  
  
## Procedures  
  
#### To add the Circ control to the dialog template  
  
1.  Load the ActiveX control container project. For this example, use the `Container` project.  
  
2.  Click the Resource View tab.  
  
3.  Open the **Dialog** folder.  
  
4.  Double-click the main dialog box template. For this example, use **IDD_CONTAINER_DIALOG**.  
  
5.  Click the Circ control icon on the Toolbox.  
  
6.  Click a spot within the dialog box to insert the Circ control.  
  
7.  From the **File** menu, choose **Save All** to save all modifications to the dialog box template.  
  
## Modifications to the Project  
 To enable the Container application to access the Circ control, Visual C++ automatically adds the wrapper class (`CCirc`) implementation file (.CPP) to the Container project and the wrapper class header (.H) file to the dialog box header file:  
  
 [!CODE [NVC_MFC_AxCont#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#1)]  
  
##  <a name="_core_the_wrapper_class_header_28h29_file"></a> The Wrapper Class Header (.H) File  
 To get and set properties (and invoke methods) for the Circ control, the `CCirc` wrapper class provides a declaration of all exposed methods and properties. In the example, these declarations are found in CIRC.H. The following sample is the portion of class `CCirc` that defines the exposed interfaces of the ActiveX control:  
  
 [!CODE [NVC_MFC_AxCont#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#2)]  
[!CODE [NVC_MFC_AxCont#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#3)]  
  
 These functions can then be called from other of the application's procedures using normal C++ syntax. For more information on using this member function set to access the control's methods and properties, see the section [Programming the ActiveX control](#_core_programming_the_activex_control).  
  
##  <a name="_core_member_variable_modifications_to_the_project"></a> Member Variable Modifications to the Project  
 Once the ActiveX control has been added to the project and embedded in a dialog box container, it can be accessed by other parts of the project. The easiest way to access the control is to [create a member variable](../vs140/ActiveX-Control-Containers--Connecting-an-ActiveX-Control-to-a-Member-Variable.md) of the dialog class, `CContainerDlg` (step 2), that is of the same type as the wrapper class added to the project by Visual C++. You can then use the member variable to access the embedded control at any time.  
  
 When the **Add Member Variable** dialog box adds the `m_circctl` member variable to the project, it also adds the following lines to the header file (.H) of the `CContainerDlg` class:  
  
 [!CODE [NVC_MFC_AxCont#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#4)]  
[!CODE [NVC_MFC_AxCont#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#5)]  
  
 In addition, a call to **DDX_Control** is automatically added to the `CContainerDlg`'s implementation of `DoDataExchange`:  
  
 [!CODE [NVC_MFC_AxCont#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#6)]  
  
##  <a name="_core_programming_the_activex_control"></a> Programming the ActiveX Control  
 At this point, you have inserted the ActiveX control into your dialog template and created a member variable for it. You can now use common C++ syntax to access the properties and methods of the embedded control.  
  
 As noted (in [The Wrapper Class Header (.H) File](#_core_the_wrapper_class_header_28h29_file)), the header file (.H) for the `CCirc` wrapper class, in this case CIRC.H, contains a list of member functions that you can use to get and set any exposed property value. Member functions for exposed methods are also available.  
  
 A common place to modify the control's properties is in the `OnInitDialog` member function of the main dialog class. This function is called just before the dialog box appears and is used to initialize its contents, including any of its controls.  
  
 The following code example uses the `m_circctl` member variable to modify the Caption and CircleShape properties of the embedded Circ control:  
  
 [!CODE [NVC_MFC_AxCont#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxCont#7)]  
  
## See Also  
 [ActiveX Control Containers](../vs140/ActiveX-Control-Containers.md)