---
title: "Adding a Class (Visual C++)"
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
ms.assetid: c34b5f70-4e72-4faa-ba21-e2b05361c4d9
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding a Class (Visual C++)
To add a class in a Visual C++ project, in **Solution Explorer**, right-click the project, click **Add**, and then click **Class**. This opens the [Add Class Dialog Box](../vs140/Add-Class-Dialog-Box.md) dialog box.  
  
 When you add a class, you must specify a name that is different from classes that already exist in MFC or ATL. If you specify a name that already exists in either library, Visual C++ displays a message that indicates that the specified name is reserved.  
  
 If your project naming convention requires you to use an existing name, then you can just change the case of one or more letters in the name because Visual C++ is case-sensitive. For example, although you cannot name a class `CDocument`, you can name it `cdocument`.  
  
## What Kind of Class Do You Want to Add?  
 In the **Add Class** dialog box, when you expand the **Visual C++** node in the left pane several groupings of installed templates are displayed. The groups include **CLR**, **ATL**, **MFC**, and **C++**. When you select a group, a list of the available templates in that group is displayed in the middle pane. Each template contains the files and source code that are required for a class.  
  
 To generate a new class, select a template in the middle pane, type a name for the class in the **Name** box, and click **Add**. This opens the **Add Class Wizard** so that you can specify options for the class.  
  
-   For more information about how to create MFC classes, see [MFC Class](../vs140/Adding-an-MFC-Class.md).  
  
-   For more information about how to create ATL classes, see [ATL Simple Object](../vs140/Adding-an-ATL-Simple-Object.md).  
  
> [!NOTE]
>  The template **Add ATL Support to MFC** does not create a class, but instead configures the project to use ATL. For more information, see [Adding ATL Support to Your MFC project](../vs140/Adding-ATL-Support-to-Your-MFC-Project.md).  
  
 To make a C++ class that does not use MFC, ATL, or CLR, use the **C++ Class** template in the **C++** group of installed templates. For more information, see [Adding a Generic C++ Class](../vs140/Adding-a-Generic-C---Class.md).  
  
 Two kinds of form-based C++ classes are available. The first one, [CFormView Class](../vs140/CFormView-Class.md) creates an MFC class. The second one creates a CLR Windows Forms class.  
  
## See Also  
 [Creating a Forms-Based MFC Application](../vs140/Creating-a-Forms-Based-MFC-Application.md)   
 [Add Class Dialog Box](../vs140/Add-Class-Dialog-Box.md)   
 [Creating Desktop Projects By Using Application Wizards](../vs140/Creating-Desktop-Projects-By-Using-Application-Wizards.md)   
 [Adding Functionality with Code Wizards](../vs140/Adding-Functionality-with-Code-Wizards--C---.md)