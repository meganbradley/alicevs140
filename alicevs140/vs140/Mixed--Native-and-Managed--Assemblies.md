---
title: "Mixed (Native and Managed) Assemblies"
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
ms.assetid: 4299dfce-392f-4933-8bf0-5da2f0d1c282
caps.latest.revision: 37
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mixed (Native and Managed) Assemblies
Mixed assemblies are capable of containing both unmanaged machine instructions and MSIL instructions. This allows them to call and be called by .NET components, while retaining compatibility with components that are entirely unmanaged. Using mixed assemblies, developers can author applications using a mixture of managed and unmanaged functionality. This makes mixed assemblies ideal for migrating existing Visual C++ applications to the .NET Platform.  
  
 For example, an existing application consisting entirely of unmanaged functions can be brought to the .NET platform by recompiling just one module with the **/clr** compiler switch. This module is then able to use .NET features, but remains compatible with the remainder of the application. In this way, an application can be converted to the .NET platform in a gradual, piece-by-piece fashion. It is even possible to decide between managed and unmanaged compilation on a function-by-function basis within the same file (see [managed, unmanaged](../vs140/managed--unmanaged.md)).  
  
 Visual C++ supports the generation of three distinct types of managed assemblies: mixed, pure, and verifiable. The latter two are discussed in [Pure & Verifiable C++ Programming](../vs140/Pure-and-Verifiable-Code--C---CLI-.md).  
  
## In This Section  
 [How To: Migrate to /clr](../vs140/How-to--Migrate-to--clr.md)  
 Describes the recommended steps for either introducing or upgrading .NET functionality in your application.  
  
 [How to: Compile MFC and ATL Code with /clr](../vs140/How-to--Compile-MFC-and-ATL-Code-By-Using--clr.md)  
 Discusses how to compile existing MFC and ATL programs to target the Common Language Runtime.  
  
 [Initialization of Mixed Assemblies](../vs140/Initialization-of-Mixed-Assemblies.md)  
 Describes the "loader lock" problem and solutions.  
  
 [Library Support for Mixed Assemblies](../vs140/Library-Support-for-Mixed-Assemblies.md)  
 Discusses how to use native libraries in **/clr** compilations.  
  
 [Performance Considerations for Interop (C++)](../vs140/Performance-Considerations-for-Interop--C---.md)  
 Describes the performance implications of mixed assemblies and data marshaling.  
  
 [Application Domains and Visual C++](../vs140/Application-Domains-and-Visual-C--.md)  
 Discusses Visual C++ support for application domains.  
  
 [Double Thunks](../vs140/Double-Thunking--C---.md)  
 Discusses the performance implications of a native entry point for a managed function.  
  
 [Avoiding Exceptions on CLR Shutdown When Consuming COM Objects Built with /clr](../vs140/Avoiding-Exceptions-on-CLR-Shutdown-When-Consuming-COM-Objects-Built-with--clr.md)  
 Discusses how to ensure proper shutdown of a managed application that consumes a COM object compiled with **/clr**.  
  
 [How to: Create a Partially Trusted Application by Removing Dependency on the CRT Library DLL](../vs140/How-to--Create-a-Partially-Trusted-Application-by-Removing-Dependency-on-the-CRT-Library-DLL.md)  
 Discusses how to create a partially trusted Common Language Runtime application using [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] by removing dependency on msvcm90.dll.  
  
 For more information about coding guidelines for mixed assemblies, see the MSDN article "An Overview of Managed/Unmanaged Code Interoperability" at [http://msdn.microsoft.com/netframework/default.aspx?pull=/library/dndotnet/html/manunmancode.asp](http://msdn.microsoft.com/netframework/default.aspx?pull=/library/dndotnet/html/manunmancode.asp).  
  
## See Also  
 [Native and .NET Interoperability](../vs140/Native-and-.NET-Interoperability.md)