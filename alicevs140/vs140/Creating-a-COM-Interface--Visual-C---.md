---
title: "Creating a COM Interface (Visual C++)"
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
ms.assetid: 1be84d3c-6886-4d1e-8493-56c4d38a96d4
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating a COM Interface (Visual C++)
Visual C++ provides wizards and templates to create projects that use COM defining interfaces and dispinterfaces for your COM objects and automation classes.  
  
 You can use these wizards to perform the following three common tasks:  
  
-   [Adding ATL Support to Your MFC Project](../vs140/Adding-ATL-Support-to-Your-MFC-Project.md)  
  
     Add ATL support to an MFC application after you create an MFC project using the [MFC Application Wizard](../vs140/MFC-Application-Wizard.md) and then running the **Add ATL Support to MFC** code wizard. This support applies only to simple COM objects added to an MFC executable or DLL project. These ATL objects may have multiple interfaces.  
  
-   [Creating an MFC ActiveX Control](../vs140/Creating-an-MFC-ActiveX-Control.md)  
  
     Open the [MFC ActiveX Control Wizard](../vs140/MFC-ActiveX-Control-Wizard.md) to create an ActiveX control with a dispinterface and an event map defined in the .idl file and the control class, respectively.  
  
-   [Adding an ATL Control](../vs140/Adding-an-ATL-Control.md)  
  
     Use a combination of the [ATL Project Wizard](../vs140/ATL-Project-Wizard.md) and the [ATL Control Wizard](../vs140/ATL-Control-Wizard.md) to create an ATL ActiveX control.  
  
     You can also add an ATL control to an MFC project to which you have added ATL support, as described above. Additionally, if you select **ATL Control** in the **Add Class** dialog box, and you have not yet added ATL support to your MFC project, Visual Studio displays a dialog box confirming adding ATL support to your MFC project.  
  
     This wizard generates IDL source and a COM map in the project classes.  
  
 Once you have an ATL project open, the [Add Class](../vs140/Add-Class-Dialog-Box.md) dialog box gives you the choice of additional wizards and templates to add COM interfaces to your project. The following wizards allow you to establish one or more interfaces for the object:  
  
-   [ATL COM+ 1.0 Component Wizard](../vs140/ATL-COM--1.0-Component-Wizard.md)  
  
-   [ATL Simple Object Wizard](../vs140/ATL-Simple-Object-Wizard.md)  
  
-   [ATL Active Server Page Component Wizard](../vs140/ATL-Active-Server-Page-Component-Wizard.md)  
  
-   [ATL Control Wizard](../vs140/ATL-Control-Wizard.md)  
  
 Additionally, you can implement new interfaces on your COM control by right-clicking the object's control class in Class View and clicking [Implement Interface](../vs140/Implement-Interface-Wizard.md).  
  
> [!NOTE]
>  Visual Studio does not provide a wizard to add an interface to a project. You can add an interface to an ATL project or to an [Adding ATL Support to Your MFC Project](../vs140/Adding-ATL-Support-to-Your-MFC-Project.md) by adding a simple object using the [ATL Simple Object Wizard](../vs140/ATL-Simple-Object-Wizard.md). Alternately, open the project's .idl file and create the interface by typing:  
  
```  
interface IMyInterface {  
};  
  
```  
  
 See [Implementing an Interface](../vs140/Implementing-an-Interface--Visual-C---.md) and [Adding Objects and Controls to an ATL Project](../vs140/Adding-Objects-and-Controls-to-an-ATL-Project.md) for more information.  
  
 Visual C++ provides several ways to view and [edit the COM interfaces](../vs140/Editing-a-COM-Interface.md) defined for your projects. [Class View](assetId:///8d7430a9-3e33-454c-a9e1-a85e3d2db925) displays icons for any interface or dispinterface defined in an .idl file in your C++ project.  
  
 For ATL-based COM object classes, Class View reads the COM map in the ATL class to display the relationship between the ATL class and any interfaces it implements.  
  
 In Class View and its shortcut menus, you can work with interfaces as follows:  
  
-   Add ATL objects to an MFC-based application.  
  
-   Add methods, properties, and events.  
  
-   Jump directly to an item's interface code by double-clicking the item.  
  
## See Also  
 [Creating Desktop Projects By Using Application Wizards](../vs140/Creating-Desktop-Projects-By-Using-Application-Wizards.md)   
 [Adding Functionality with Code Wizards](../vs140/Adding-Functionality-with-Code-Wizards--C---.md)