---
title: "How to: Activate and Use a Windows Runtime Component Using WRL"
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
ms.assetid: 54828f02-6af3-45d1-b965-d0104442f8d5
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Activate and Use a Windows Runtime Component Using WRL
This document shows how to use the [!INCLUDE[cppwrl](../vs140/includes/cppwrl_md.md)] ([!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)]) to initialize the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] and how to activate and use a [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] component.  
  
> [!NOTE]
>  This example activates a built-in [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] component. To learn how to create your own component that you can activate in a similar manner, see [Walkthrough: Creating a Basic Windows Runtime Component Using WRL](../vs140/Walkthrough--Creating-a-Basic-Windows-Runtime-Component-Using-WRL.md).  
  
 To use a component, you must acquire an interface pointer to the type that is implemented by the component. And because the underlying technology of the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] is the Component Object Model (COM), you must follow COM rules to maintain an instance of the type. For example, you must maintain the *reference count* that determines when the type is deleted from memory.  
  
 To simplify the use of the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)], [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] provides the smart pointer template, [ComPtr<T\>](../vs140/ComPtr-Class.md), that automatically performs reference counting. When you declare a variable, specify `ComPtr<`*interface-name*`>` *identifier*. To access an interface member, apply the arrow member-access operator (`->`) to the identifier.  
  
> [!IMPORTANT]
>  When you call an interface function, always test the `HRESULT` return value.  
  
## Activating and Using a Windows Runtime Component  
 The following steps use the `Windows::Foundation::IUriRuntimeClass` interface to demonstrate how to create an activation factory for a [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] component, create an instance of that component, and retrieve a property value. They also show how to initialize the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. The complete example follows.  
  
> [!IMPORTANT]
>  Although you typically use the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)] in a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] app, this example uses a console app for illustration. Functions such as `wprintf_s` are not available from a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] app. For more information about the types and functions that you can use in a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] app, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx) and [Win32 and COM for Windows Store apps](http://msdn.microsoft.com/library/windows/apps/br205757.aspx).  
  
#### To activate and use a Windows Runtime component  
  
1.  Include (`#include`) any required [!INCLUDE[wrt](../vs140/includes/wrt_md.md)], [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)], or standard C++ library headers.  
  
     [!CODE [wrl-consume-component#2](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#2)]  
  
     We recommend that you utilize the `using namespace` directive in your .cpp file to make the code more readable.  
  
2.  Initialize the thread in which the app executes. Every app must initialize its thread and threading model. This example uses the [Microsoft::WRL::Wrappers::RoInitializeWrapper](../vs140/RoInitializeWrapper-Class.md) class to initialize the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] and specifies [RO_INIT_MULTITHREADED](http://msdn.microsoft.com/library/windows/apps/br224661.aspx) as the threading model. The `RoInitializeWrapper` class calls `Windows::Foundation::Initialize` at construction, and `Windows::Foundation::Uninitialize` when it is destroyed.  
  
     [!CODE [wrl-consume-component#3](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#3)]  
  
     In the second statement, the [RoInitializeWrapper::HRESULT](../vs140/RoInitializeWrapper--HRESULT---Operator.md) operator returns the `HRESULT` from the call to `Windows::Foundation::Initialize`.  
  
3.  Create an *activation factory* for the `ABI::Windows::Foundation::IUriRuntimeClassFactory` interface.  
  
     [!CODE [wrl-consume-component#4](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#4)]  
  
     The [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] uses fully-qualified names to identify types. The `RuntimeClass_Windows_Foundation_Uri` parameter is a string that's provided by the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] and contains the required runtime class name.  
  
4.  Initialize a [Microsoft::WRL::Wrappers::HString](../vs140/HString-Class.md) variable that represents the URI `"http://www.microsoft.com"`.  
  
     [!CODE [wrl-consume-component#6](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#6)]  
  
     In the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)], you don’t allocate memory for a string that the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] will use. Instead, the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] creates a copy of your string in a buffer that it maintains and uses for operations, and then returns a handle to the buffer that it created.  
  
5.  Use the `IUriRuntimeClassFactory::CreateUri` factory method to create a `ABI::Windows::Foundation::IUriRuntimeClass` object.  
  
     [!CODE [wrl-consume-component#7](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#7)]  
  
6.  Call the `IUriRuntimeClass::get_Domain` method to retrieve the value of the `Domain` property.  
  
     [!CODE [wrl-consume-component#8](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#8)]  
  
7.  Print the domain name to the console and return. All `ComPtr` and RAII objects leave scope and are released automatically.  
  
     [!CODE [wrl-consume-component#9](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#9)]  
  
     The [WindowsGetStringRawBuffer](http://msdn.microsoft.com/library/windows/apps/br224636.aspx) function retrieves the underlying Unicode form of the URI string.  
  
 Here's the complete example:  
  
 [!CODE [wrl-consume-component#1](../CodeSnippet/VS_Snippets_Misc/wrl-consume-component#1)]  
  
## Compiling the Code  
 To compile the code, copy it and then paste it in a Visual Studio project, or paste it in a file that is named `wrl-consume-component.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe wrl-consume-component.cpp runtimeobject.lib**  
  
## See Also  
 [Windows Runtime C++ Template Library](../vs140/Windows-Runtime-C---Template-Library--WRL-.md)