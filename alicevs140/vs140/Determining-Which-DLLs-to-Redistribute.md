---
title: "Determining Which DLLs to Redistribute"
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
ms.assetid: f7a2cb42-fb48-42ab-abd2-b35e2fd5601a
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Determining Which DLLs to Redistribute
When you build an application that uses DLLs supplied by Visual Studio, users of your application must also have those DLLs on their computers for the application to run. Because most users probably do not have Visual Studio installed, you must provide these DLLs for them. Visual Studio makes these DLLs available as redistributable libraries that you can include in your application installer.  
  
 The redistributable DLLs are included with your installation of Visual Studio. By default, they are installed in the Program Files (x86)\Microsoft Visual Studio version\VC\Redist folder. To make it easier to include them with your installer, they are also available as stand-alone redistributable packages from the Microsoft Download Center. These are executables that install the redistributable files on a user's computer. The version of the redistributable package must match the version of the Visual Studio toolset used to create your application. To find a matching redistributable package, search the [Microsoft Download Center](http://go.microsoft.com/fwlink/p/?LinkId=158431) for "Visual C++ Redistributable Packages".  
  
 To determine which DLLs you have to redistribute with your application, collect a list of the DLLs that your application depends on. One way to collect the list is to run Dependency Walker (depends.exe), as described in [Understanding Dependencies of a Visual C++ Application](../vs140/Understanding-the-Dependencies-of-a-Visual-C---Application.md).  
  
 When you have the list of dependencies, compare it to the list in any Redist.txt file in the Microsoft Visual Studio installation directory, or to the "REDIST list" of redistributable DLLs that is referenced in the "Distributable Code" section of the Microsoft Software License Terms for your copy of Visual Studio. For Visual Studio 2013, the list is available online in [Distributable Code for Microsoft Visual Studio 2013 and Microsoft Visual Studio 2013 SDK](http://go.microsoft.com/fwlink/p/?LinkId=313603). You cannot redistribute all of the files that are included in Visual Studio; you are only permitted to redistribute the files that are specified in Redist.txt or the online "REDIST list." Debug versions of applications and the various Visual C++ debug DLLs are not redistributable. For more information, see [Choosing a Deployment Method](../vs140/Choosing-a-Deployment-Method.md).  
  
 The following table describes some of the Visual C++ DLLs that your application might depend on.  
  
|Visual C++ Library|Description|Applies to|  
|--------------------------|-----------------|----------------|  
|msvcr*version*.dll|C Runtime Library (CRT) for native code.|Applications that use the [C Run-Time Libraries](../vs140/CRT-Library-Features.md).|  
|msvcp*version*.dll|Standard C++ Library for native code.|Applications that use the [Standard C++ Library](../vs140/C---Standard-Library-Reference.md).|  
|mfc*version*.dll|Microsoft Foundation Classes (MFC) Library.|Applications that use the [MFC Library](../vs140/MFC-Desktop-Applications.md).|  
|mfc*version*u.dll|MFC Library with Unicode support.|Applications that use the [MFC Library](../vs140/MFC-Desktop-Applications.md) and require Unicode support.|  
|mfcmifc80.dll|MFC Managed Interfaces Library.|Applications that use the [MFC Library](../vs140/MFC-Desktop-Applications.md) with [Windows Forms Controls](assetId:///f050de8f-4ebd-4042-94b8-edf9a1dbd52a).|  
|mfcm*version*.dll|MFC Managed Library.|Applications that use the [MFC Library](../vs140/MFC-Desktop-Applications.md) with [Windows Forms Controls](assetId:///f050de8f-4ebd-4042-94b8-edf9a1dbd52a).|  
|mfcm*version*u.dll|MFC Managed Library with Unicode support.|Applications that use the [MFC Library](../vs140/MFC-Desktop-Applications.md) with [Windows Forms Controls](assetId:///f050de8f-4ebd-4042-94b8-edf9a1dbd52a) and require Unicode support.|  
  
> [!NOTE]
>  You no longer need to redistribute the Active Template Library as a separate DLL. Its functionality has been moved to headers and a static library.  
  
 For more information about how to redistribute these DLLs with your application, see [Redistributing Visual C++ Files](../vs140/Redistributing-Visual-C---Files.md). For examples, see [Deployment Examples](../vs140/Deployment-Examples.md).  
  
 Typically, you do not have to redistribute system DLLs because they are part of the operating system. However, there might be exceptions, for example, when your application will run on several versions of Microsoft operating systems. In this case, be sure to read the corresponding license terms. Also, try to get the system DLLs upgraded either through Windows Update, service packs or by using redistributable packages made available by Microsoft. You may be able to locate available packages by searching on the [Microsoft Support](http://support.microsoft.com/) website or the [Microsoft Download Center](http://go.microsoft.com/fwlink/p/?LinkId=158431).  
  
## See Also  
 [Choosing a Deployment Method](../vs140/Choosing-a-Deployment-Method.md)   
 [Deployment (C++)](../vs140/Deploying-Native-Desktop-Applications--Visual-C---.md)