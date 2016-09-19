---
title: "ATL Module Classes"
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
ms.assetid: fd75382d-c955-46ba-a38e-37728b7fa00f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Module Classes
This topic discusses the module classes that were new in ATL 7.0.  
  
## CComModule Replacement Classes  
 Earlier versions of ATL used `CComModule`. In ATL 7.0, `CComModule` functionality is replaced by several classes:  
  
-   [CAtlBaseModule](../vs140/CAtlBaseModule-Class.md) Contains information required by most applications that use ATL. Contains the HINSTANCE of the module and the resource instance.  
  
-   [CAtlComModule](../vs140/CAtlComModule-Class.md) Contains information required by the COM classes in ATL.  
  
-   [CAtlWinModule](../vs140/CAtlWinModule-Class.md) Contains information required by the windowing classes in ATL.  
  
-   [CAtlDebugInterfacesModule](../vs140/CAtlDebugInterfacesModule-Class.md) Contains support for interface debugging.  
  
-   [CAtlModule](../vs140/CAtlModule-Class.md) The following `CAtlModule`-derived classes are customized to contain information required in a particular application type. Most members in these classes can be overridden:  
  
    -   [CAtlDllModuleT](../vs140/CAtlDllModuleT-Class.md) Used in DLL applications. Provides code for the standard exports.  
  
    -   [CAtlExeModuleT](../vs140/CAtlExeModuleT-Class.md) Used in EXE applications. Provides code required in an EXE.  
  
    -   [CAtlServiceModuleT](../vs140/CAtlServiceModuleT-Class.md) Provides support to create Windows NT and Windows 2000 Services.  
  
 `CComModule` is still available for backward compatibility.  
  
## Reasons for Distributing CComModule Functionality  
 The functionality of `CComModule` was distributed into several new classes for the following reasons:  
  
-   Make the functionality in `CComModule` granular.  
  
     Support for COM, windowing, interface debugging, and application-specific (DLL or EXE) features is now in separate classes.  
  
-   Automatically declare global instance of each of these modules.  
  
     A global instance of the required module classes is linked into the project.  
  
-   Remove the necessity of calling Init and Term methods.  
  
     Init and Term methods have moved into the constructors and destructors for the module classes; there is no longer a need to call Init and Term.  
  
## See Also  
 [Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)