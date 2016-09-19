---
title: "ATL Property Page Wizard"
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
ms.assetid: 6113e325-facd-4f68-b491-144d75209922
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Property Page Wizard
This wizard [adds a property page into an ATL project](../vs140/Adding-an-ATL-Property-Page.md) or to an MFC project with ATL support. An ATL property page provides a user interface for setting the properties (or calling the methods) of one or more COM objects.  
  
## Remarks  
 Beginning with [!INCLUDE[vs_orcas_long](../vs140/includes/vs_orcas_long_md.md)], the registration script produced by this wizard will register its COM components under **HKEY_CURRENT_USER** instead of **HKEY_LOCAL_MACHINE**. To modify this behavior, set the **Register component for all users** option of the ATL Wizard.  
  
## Names  
 Specify the names for the object, interface, and classes to be added to your project. Except for **Short name**, all other boxes can be edited independently. If you change the text for **Short name**, the change is reflected in the names of all other boxes in this page. If you change the **Coclass** name in the COM section, the change is reflected in the **Type** and **ProgID** boxes. This naming behavior is designed to make all the names easily identifiable for you as you develop your property page.  
  
> [!NOTE]
>  **Coclass** is editable on only nonattributed projects. If your project attributed, you cannot edit **Coclass**.  
  
### C++  
 Provides information for the C++ class created to implement the object.  
  
|||  
|-|-|  
|Term|Definition|  
|**Short name**|Sets the abbreviated name for the object. The name that you provide determines the class and **Coclass** names, the file (**.cpp** and **.h**) names, the **Type** name, and the **ProgID**, unless you change those fields individually.|  
|**.h file**|Sets the name of the header file for the new object's class. By default, this name is based on the name that you provide in **Short name**. Click the ellipsis button to save the file name to the location of your choice, or to append the class declaration to an existing file. If you select an existing file, the wizard will not save it to the selected location until you click **Finish** in the wizard.<br /><br /> The wizard does not overwrite a file. If you select the name of an existing file, when you click **Finish**, the wizard prompts you to indicate whether the class declaration should be appended to the contents of the file. Click **Yes** to append the file; click **No** to return to the wizard and specify another file name.|  
|**Class**|Sets the name of the class that implements the object. This name is based on the name that you provide in **Short name**, preceded by 'C', the typical prefix for a class name.|  
|**.cpp file**|Sets the name of the implementation file for the new object's class. By default, this name is based on the name that you provide in **Short name**. Click the ellipsis button to save the file name to the location of your choice. The file is not saved to the selected location until you click **Finish** in the wizard.<br /><br /> The wizard does not overwrite a file. If you select the name of an existing file, when you click **Finish**, the wizard prompts you to indicate whether the class implementation should be appended to the contents of the file. Click **Yes** to append the file; click **No** to return to the wizard and specify another file name.|  
|**Attributed**|Indicates whether the object uses attributes. If you are adding an object to an attributed ATL project, this option is selected and not available to change, that is, you can add only attributed objects to a project created with attribute support.<br /><br /> You can add an attributed object only to an ATL project that uses attributes. If you select this option for an ATL project that does not have attribute support, the wizard prompts you to specify whether you want to add attribute support to the project.<br /><br /> By default, any objects you add after you set this option are designated as attributed (the check box is selected). You can clear this box to add an object that does not use attributes.<br /><br /> See [Application Settings, ATL Project Wizard](../vs140/Application-Settings--ATL-Project-Wizard.md) and [Basic Mechanics of Attributes](../vs140/Basic-Mechanics-of-Attributes.md) for more information.|  
  
### COM  
 Provides information about the COM functionality for the object.  
  
 **Coclass**  
 Sets the name of the component class that contains a list of interfaces supported by the object.  
  
> [!NOTE]
>  If you create your project using attributes, or if you indicate on this wizard page that the property page uses attributes, you cannot change this option because ATL does not include the `coclass` attribute.  
  
 **Type**  
 Sets the object description that will appear in the registry  
  
 **ProgID**  
 Sets the name that containers can use instead of the CLSID of the object.  
  
## See Also  
 [Options, ATL Property Page Wizard](../vs140/Options--ATL-Property-Page-Wizard.md)   
 [Strings, ATL Property Page Wizard](../vs140/Strings--ATL-Property-Page-Wizard.md)   
 [Example: Implementing a Property Page](../vs140/Example--Implementing-a-Property-Page.md)