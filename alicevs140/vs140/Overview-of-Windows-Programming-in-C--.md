---
title: "Overview of Windows Programming in C++"
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
ms.assetid: efc691d7-21f3-47ae-ae56-cab999ccf59d
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overview of Windows Programming in C++
You can use Visual C++ to write a wide variety of programs that run on a Windows PC (x86, x64 or ARM), on a Windows server, in the cloud, or on Xbox. Well-written C++ programs are fast, efficient, economical in power consumption, and able to take full advantage of multicore and many-core devices, general computing on the graphics processing unit (GPGPU), and other recent advances in hardware.  
  
 There are several broad categories of Windows apps that you can develop with Visual C++. These categories have different programming models, or app models, which means that they use different libraries and APIs that provide access to the platform and provide user interface.  
  
-   [Windows Universal apps](#BK_WindowsUniversal). The third category of Windows apps was introduced with Windows 8, and support for this category of apps continues in Windows 10. These apps are frequently referred to as just "Windows apps" and they include desktop and mobile apps that target a variety of devices. You can write these apps in C++/CX, a dialect of C++ that includes support for Windows Runtime development, or in standard C++ with COM using the Windows Runtime Library (WRL). These apps were originally designed to run full-screen, although in Windows 10 users have the option of running them in a desktop window. These apps are touch-oriented, but it is easy to use the mouse to operate if users prefer or if a touch screen is not available. These apps are distributed from the Windows Store, a fact which led to them being called "Windows Store apps."  
  
-   [Desktop, Server, and Cloud Applications and Games](#BK_Native). This category includes Windows Desktop applications, sometimes called Win32 applications since these applications were using the Win32 API on Prior to Windows 8, all Windows applications were in this category. Applications in this category can use MFC for a user interface and ATL to interact with Windows components, which are typically COM objects.  
  
     Applications, components, or libraries written with standard C++ also fit into this category.  
  
     This category also includes using C++ for core components and computational code in the context of server and cloud programming. Sometimes the performance-intensive code at the core of a server or cloud application is written in C++ to maximize performance. You can compile such code into a DLL and use it from C# or Visual Basic.  
  
-   **.NET Framework applications**. Most .NET Framework applications are written in C# or Visual Basic, but you can also C++/CLI (the /clr compiler option in Visual C++). We recommend using C++/CLI for a minimal interop layer in a larger application that includes managed and native code.  
  
##  <a name="BK_WindowsUniversal"></a> Windows Universal Apps  
 With Windows 10, apps are able to run on all Windows 10 devices such as tablets and mobile phones, as well as on the desktop. On the desktop, they are able to run as a desktop window, instead of always running full-screen. These apps can also run on the Xbox, and on future devices.  The programming model for the two types of apps is different from Win32 desktop applications. These Windows apps run on the Windows Runtime, which provides user interface elements, essential services for these apps and provides, and an interface to the diverse hardware devices that are supported. These apps compile to native code and have a XAML user interface, or use DirectX. You can also write [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] components in native code that other Windows apps can consume—these include apps that are written in C#, Visual Basic, or JavaScript. For more information, see [Create your first Windows Store app using C++](http://go.microsoft.com/fwlink/?LinkID=534976), [Create your first Windows Store game using DirectX](http://go.microsoft.com/fwlink/p/?LinkId=244656), and [Creating Windows Runtime components in C++](http://go.microsoft.com/fwlink/p/?LinkId=244658).  
  
 For Universal Windows Platform samples, see [Windows Universal Samples on GitHub](https://github.com/Microsoft/Windows-universal-samples)  
  
 If you have an existing Windows 8.1 project and want to port it to Windows 10, see [Porting to the Universal Windows Platform (C++)](../vs140/Porting-to-the-Universal-Windows-Platform--C---.md). If you have existing classic Win32 desktop libraries and code that you want to integrate into a UWP app, see [How to: Use Existing C++ Code in Universal Windows Platform Apps](../vs140/How-to--Use-Existing-C---Code-in-a-Universal-Windows-Platform-App.md).  
  
 You can also write Universal Windows apps, games, and components without using the [!INCLUDE[cppwrt](../vs140/includes/cppwrt_md.md)] ([!INCLUDE[cppwrt_short](../vs140/includes/cppwrt_short_md.md)]); instead, you can use the [!INCLUDE[cppwrl](../vs140/includes/cppwrl_md.md)] ([!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)]). For more information, see [Windows Runtime C++ Template Library](../vs140/Windows-Runtime-C---Template-Library--WRL-.md).  
  
 With [!INCLUDE[cpp_dev14_long](../vs140/includes/cpp_dev14_long_md.md)], you can develop Universal Windows apps that run on Windows 10 desktop and mobile devices. You can also develop Windows 8.1 apps and Windows Phone 8.1 apps in [!INCLUDE[cpp_dev14_long](../vs140/includes/cpp_dev14_long_md.md)], but to do so, you must first install Visual Studio 2013 on the same computer, and then configure your project to use the **Visual Studio 2013 (v120)** toolset. To configure this setting in your project, open the project's properties and in the **General** section, set the **Platform Toolset** to **Visual Studio 2013 (v120)**.  
  
 If you install the Phone 8.0 tools in Visual Studio setup, you can also target Windows Phone 8.0.  
  
 A new concept introduced in Windows 10 called API Contracts replaces the old practice of targeting specific Windows versions. Instead, you can choose which API Contracts your app needs and it will then run on any Windows device that supports those contracts. An API contract is a set of stable APIs that provide access to platform or device resources. API Contracts can be included as references in the project system. In a Visual Studio project, if you add a reference to a particular Extension SDK, then Visual Studio adds the appropriate API Contracts.  
  
 For more information on all of these concepts, see [Guide to Windows Universal Apps](http://go.microsoft.com/fwlink/?LinkId=534605).  
  
##  <a name="BK_Win32"></a> Desktop, Server, and Cloud Apps and Games  
 In the cloud you can write Azure native code assemblies in C++ and call into them from Web Roles that are created in C#. For more information, see [Azure SDK](http://go.microsoft.com/fwlink/p/?LinkId=256416).  
  
 To learn the basics of writing Windows client applications for the desktop, see [Developing Windows Applications in C++](http://msdn.microsoft.com/vstudio//hh304489) and [Introduction to Windows Programming in C++](http://msdn.microsoft.com/library/windows/desktop/ff381398\(v=vs.85\).aspx).  
  
 On Windows 10, you can use Visual C++ to create many kinds of programs:  
  
-   Command-line apps and utilities. For more information, see [Console Applications in Visual C++](../vs140/Console-Applications-in-Visual-C--.md).  
  
-   DirectX Games that run on the PC or Xbox. For more information, see [DirectX Developer Center](http://go.microsoft.com/fwlink/p/?LinkId=256418).  
  
-   Consumer applications that have sophisticated graphical user interfaces. For more information, see [Hilo: Developing C++ Applications for Windows](http://go.microsoft.com/fwlink/p/?LinkId=256417)  
  
-   Enterprise and line-of-business apps that run on the .NET Framework, or serve as a bridge between .NET Framework apps and apps or components that are written in native code. For more information, see [.NET Programming in Visual C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md).  
  
-   SQL database clients that run in native code. For more information, see [SQL Server Native Client](http://go.microsoft.com/fwlink/p/?LinkId=256419).  
  
-   Add-ins for Microsoft Office applications. For more information, see [Building a C++ Add-in for Outlook 2010](http://go.microsoft.com/fwlink/p/?LinkId=256420)  
  
-   Device drivers. For more information, see [Windows Driver Kit (WDK)](http://go.microsoft.com/fwlink/p/?LinkId=256421)  
  
-   Windows services. For more information, see [Introduction to Windows Service Applications](assetId:///1b1b5e67-3ff3-40c0-8154-322cfd6ef0ae).  
  
 You can use Visual C++ to package almost any kind of custom high-performance functionality in Win32 DLLs or in COM DLLs that can be consumed by C++ apps or by apps that are written in other languages—for example, C# or Visual Basic. For more information about WIn32 DLLs, see [DLLs in Visual C++](../vs140/DLLs-in-Visual-C--.md). For more information about COM development, see [Component Object Model (COM)](assetId:///375d29a7-a1f3-4bd8-8621-bad7a049b2aa).  
  
## SDKs and Header Files  
 Visual C++ includes the C and C++ standard libraries, the Standard Template Library (STL), and other Microsoft-specific libraries. The include folders that contain header files for these libraries are either located in the Visual Studio installation directory under the \VC\  folder, or in the case of the C Runtime (CRT) Library, Windows SDK installation folder, for example, Windows Kits\10 in your Program Files folder for the Windows 10 SDK.  The Microsoft  libraries include:  
  
-   Microsoft Foundation Classes (MFC): An object-oriented framework for creating traditional Windows programs—especially enterprise applications—that have rich user interfaces that feature buttons, list boxes, tree views, and other controls. For more information, see [MFC Desktop Applications](../vs140/MFC-Desktop-Applications.md).  
  
-   Active Template Library (ATL): A powerful helper library for creating COM components. For more information, see [ATL COM Desktop Components](../vs140/ATL-COM-Desktop-Components.md).  
  
-   C++ AMP (C++ Accelerated Massive Parallelism): A library that enables high-performance general computational work on the GPU. For more information, see [C++ AMP (C++ Accelerated Massive Parallelism)](../vs140/C---AMP--C---Accelerated-Massive-Parallelism-.md).  
  
-   Concurrency Runtime: A library that simplifies the work of parallel and asynchronous programming for multicore and many-core devices. For more information, see [Concurrency Runtime](../vs140/Concurrency-Runtime.md).  
  
 Many Windows programming scenarios also require the Windows SDK, which includes the header files that enable access to the Windows operating system components. By default, all editions of [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)] install the Windows SDK, which enables development of Universal Windows apps. To develop Universal Windows apps for Windows 10, you need the Windows 10 version of the Windows SDK. For information about the Windows 10 SDK, see [Windows 10 SDK](http://go.microsoft.com/fwlink/p/?LinkId=534603). (For more information about the Windows SDKs for earlier versions of Windows, see [Overview of the Windows SDK](assetId:///9a2db508-5b77-43f8-afa4-1ca82d24bb83)).  
  
 Other platforms such as Xbox and Azure have their own SDKs that you may have to install. For more information, see the DirectX Developer Center and the Azure Developer Center.  
  
## Development Tools  
 Visual Studio includes a powerful debugger for native code, static analysis tools, graphics debugging tools, a full-featured code editor, support for unit tests, and many other tools and utilities. For more information, see [Application Development in Visual Studio](assetId:///97490c1b-a247-41fb-8f2c-bc4c201eff68), and [Tools for Visual C++ Development](../vs140/IDE-and-Tools-for-Visual-C---Development.md).  
  
## Related Articles  
  
|Title|Description|  
|-----------|-----------------|  
|[Visual C++](../vs140/Visual-C---in-Visual-Studio-2015.md)|Parent topic for MSDN Library content about C++.|