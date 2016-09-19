---
title: "How to: Create a Classic COM Component Using WRL"
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
ms.assetid: 5efe7690-90d5-4c3c-9e53-11a14cefcb19
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Classic COM Component Using WRL
You can use the [!INCLUDE[cppwrl](../vs140/includes/cppwrl_md.md)] ([!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)]) to create basic classic COM components for use in desktop apps, in addition to using it for [!INCLUDE[win8_appstore_long](../vs140/includes/win8_appstore_long_md.md)] apps. For the creation of COM components, the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] may require less code than the ATL. For information about the subset of COM that the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] supports, see [Windows Runtime C++ Template Library (WRL)](../vs140/Windows-Runtime-C---Template-Library--WRL-.md).  
  
 This document shows how to use the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] to create a basic COM component. Although you can use the deployment mechanism that best fits your needs, this document also shows a basic way to register and consume the COM component from a desktop app.  
  
### To use the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] to create a basic classic COM component  
  
1.  In Visual Studio, create a **Blank Solution** project. Name the project, for example, `WRLClassicCOM`.  
  
2.  Add a **Win32 Project** to the solution. Name the project, for example, `CalculatorComponent`. On the **Application Settings** tab, select **DLL**.  
  
3.  Add a **Midl File (.idl)** file to the project. Name the file, for example, `CalculatorComponent.idl`.  
  
4.  Add this code to CalculatorComponent.idl:  
  
     [!CODE [wrl-classic-com-component#1](../CodeSnippet/VS_Snippets_Misc/wrl-classic-com-component#1)]  
  
5.  In CalculatorComponent.cpp, define the `CalculatorComponent` class. The `CalculatorComponent` class inherits from [Microsoft::WRL::RuntimeClass](../vs140/RuntimeClass-Class.md). [Microsoft::WRL::RuntimeClassFlags<ClassicCom\>](../vs140/RuntimeClassFlags-Structure.md) specifies that the class derives from [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509\(v=vs.85\).aspx) and not [IInspectable](http://msdn.microsoft.com/library/br205821\(v=vs.85\).aspx). (`IInspectable` is available only to [!INCLUDE[win8_appstore_short](../vs140/includes/win8_appstore_short_md.md)] app components.) `CoCreatableClass` creates a factory for the class that can be used with functions such as [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615\(v=vs.85\).aspx).  
  
     [!CODE [wrl-classic-com-component#2](../CodeSnippet/VS_Snippets_Misc/wrl-classic-com-component#2)]  
  
6.  Use the following code to replace the code in dllmain.cpp. This file defines the DLL export functions. These functions use the [Microsoft::WRL::Module](../vs140/Module-Class.md) class to manage the class factories for the module.  
  
     [!CODE [wrl-classic-com-component#3](../CodeSnippet/VS_Snippets_Misc/wrl-classic-com-component#3)]  
  
7.  Add a **Module-Definition File (.def)** file to the project. Name the file, for example, `CalculatorComponent.def`. This file gives the linker the names of the functions to be exported.  
  
8.  Add this code to CalculatorComponent.def:  
  
     [!CODE [wrl-classic-com-component#4](../CodeSnippet/VS_Snippets_Misc/wrl-classic-com-component#4)]  
  
9. Add runtimeobject.lib to the linker line. To learn how, see [.Lib Files as Linker Input](../vs140/.Lib-Files-as-Linker-Input.md).  
  
### To consume the COM component from a desktop app  
  
1.  Register the COM component with the Windows Registry. To do so, create a registration entries file, name it `RegScript.reg`, and add the following text. Replace *<dll-path>* with the path of your DLL—for example, `C:\\temp\\WRLClassicCOM\\Debug\\CalculatorComponent.dll`.  
  
     [!CODE [wrl-classic-com-component#5](../CodeSnippet/VS_Snippets_Misc/wrl-classic-com-component#5)]  
  
2.  Run RegScript.reg or add it to your project’s **Post-Build Event**. For more information, see [Pre-build Event/Post-build Event Command Line Dialog Box](../vs140/Pre-build-Event-Post-build-Event-Command-Line-Dialog-Box.md).  
  
3.  Add a **Win32 Console Application** project to the solution. Name the project, for example, `Calculator`.  
  
4.  Use this code to replace the contents of Calculator.cpp:  
  
     [!CODE [wrl-classic-com-component#6](../CodeSnippet/VS_Snippets_Misc/wrl-classic-com-component#6)]  
  
## Robust Programming  
 This document uses standard COM functions to demonstrate that you can use the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] to author a COM component and make it available to any COM-enabled technology. You can also use [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] types such as [Microsoft::WRL::ComPtr](../vs140/ComPtr-Class.md) in your desktop app to manage the lifetime of COM and other objects. The following code uses the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] to manage the lifetime of the `ICalculatorComponent` pointer. The `CoInitializeWrapper` class is an RAII wrapper that guarantees that the COM library is freed and also guarantees that the lifetime of the COM library outlives the `ComPtr` smart pointer object.  
  
 [!CODE [wrl-classic-com-component#7](../CodeSnippet/VS_Snippets_Misc/wrl-classic-com-component#7)]  
  
## See Also  
 [Windows Runtime C++ Template Library (WRL)](../vs140/Windows-Runtime-C---Template-Library--WRL-.md)