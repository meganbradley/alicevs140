---
title: "WRL Class Library Project Template"
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
ms.assetid: 628b0852-89e5-44f8-bf58-a09762bda15c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WRL Class Library Project Template
If you use Visual Studio to write a [!INCLUDE[cppwrl](../vs140/includes/cppwrl_md.md)] ([!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)]) project, you can greatly simplify your task by downloading the WRL Class Library project template.  
  
> [!NOTE]
>  If you have to manually update the project settings for an existing project, see [DLLs (C++/CX)](http://msdn.microsoft.com/library/windows/apps/hh699881\(v=vs.110\).aspx).  
  
## Download the WRL Project Template  
 Visual Studio doesn't provide a template for [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] projects. Here’s how to download a project template that creates a basic class library for [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps with [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)].  
  
#### To download the WRL Project Template  
  
1.  On the menu bar, choose **File**, **New Project**.  
  
2.  In the left pane of the **New Project** dialog box, select **Online**, and then select **Templates**.  
  
3.  In the **Search online templates** box in the upper right corner, type `WRL Class Library`. When the template appears in the search results, choose the **OK** button.  
  
4.  In the **Download and Install** dialog box, if you agree to the licensing terms, choose the **Install** button.  
  
5.  After the template installs, create a project by choosing **File**, **New Project**, and then selecting the `WRLClassLibrary` template. The project creates a DLL.  
  
## Examples that use the project template  
 Read [Walkthrough: Creating a Basic Windows Runtime Component (WRL)](../vs140/Walkthrough--Creating-a-Basic-Windows-Runtime-Component-Using-WRL.md) for an example that uses this template to create a [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] component.  
  
## What the project template provides  
 The project template provides:  
  
-   an .idl file that declares the MIDL attributes for a basic interface its class implementation. Here’s an example.  
  
     [!CODE [wrl-project-template#1](../CodeSnippet/VS_Snippets_Misc/wrl-project-template#1)]  
  
-   a .cpp file that defines the class implementation. Here’s an example.  
  
     [!CODE [wrl-project-template#2](../CodeSnippet/VS_Snippets_Misc/wrl-project-template#2)]  
  
     The [RuntimeClass](../vs140/RuntimeClass-Class.md) base class helps manage the global reference of all objects in the module and declares the methods of the [IUnknown](assetId:///33f1d79a-33fc-4ce5-a372-e08bda378332) and [IInspectable](assetId:///0657e51f-d4c0-46c6-927d-b01e54b6846c) interfaces. The [InspectableClass](../vs140/InspectableClass-Macro.md) macro implements `IUnknown` and `IInspectable`. The [ActivatableClass](../vs140/ActivatableClass-Macros.md) macro creates a class factory that creates instances of the class.  
  
-   a file named module.cpp that defines the library exports `DllMain`, `DllCanUnloadNow`, `DllGetActivationFactory`, and `DllGetClassObject`.  
  
## See Also  
 [Windows Runtime C++ Template Library](../vs140/Windows-Runtime-C---Template-Library--WRL-.md)