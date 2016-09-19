---
title: "How to: Migrate to -clr:pure (C++-CLI)"
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
H1: How to: Migrate to /clr:pure (C++/CLI)
ms.assetid: 5ffb1184-2095-4ade-84aa-4fa6324bc764
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Migrate to -clr:pure (C++-CLI)
This topic discusses issues likely to arise when migrating to pure MSIL using **/clr:pure** (see [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) for more information). This topic assumes that the code being migrated is currently complied as mixed assembly using the **/clr** option, as the migration path from unmanaged code to pure MSIL is not a direct one. For unmanaged code, see [How To: Migrate to /clr](../vs140/How-to--Migrate-to--clr.md) before attempting to migrate to pure MSIL.  
  
## Basic Changes  
 Pure MSIL is comprised of MSIL instructions, so code containing functions that cannot be expressed in MSIL will prevent compilation. This includes functions defined as using calling conventions other than [__clrcall](../Topic/__clrcall.md). (Non __clrcall functions can be invoked in a pure MSIL component, but not defined.)  
  
 To ensure no runtime errors, you should enable the C4412 warning. Enable C4412 by adding `#pragma warning (default : 4412)` to each compiland that you compile with **/clr:pure** and that passes C++ types to and from IJW (**/clr)** or native code. See [Compiler Warning (level 2) C4412](../vs140/Compiler-Warning--level-2--C4412.md) for more information.  
  
## Architectural Considerations  
 Some of the limitations of pure MSIL assemblies listed in [Pure and Verifiable Code](../vs140/Pure-and-Verifiable-Code--C---CLI-.md) have high-level implications for application design and migration strategy. Most notably, unlike mixed assemblies, pure MSIL assemblies don't enjoy full compatibility with unmanaged modules.  
  
 Pure MSIL assemblies can call unmanaged functions, but cannot be called by unmanaged functions. As a result, pure MSIL is a better candidate for client code that uses unmanaged functions than it is for server code that is used by unmanaged functions. If functionality contained in a pure MSIL assembly is to be used by unmanaged functions, a mixed assembly must be used as an interface layer.  
  
 Applications that use ATL or MFC are not good candidates for migration to pure MSIL, as these libraries are not supported in this release. Likewise, the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] contains header files that do not compile under **/clr:pure**.  
  
 While pure MSIL assemblies can call unmanaged functions, this ability is limited to simple C-style functions. The use of more complex unmanaged APIs is likely to require the unmanaged functionality to be exposed in the form of a COM interface, or a mixed assembly that can act as an interface between the pure MSIL and unmanaged components. Using a mixed assembly layer is the only way to use unmanaged functions that take callback functions, for example, as a pure assembly is unable to provide a native callable function for use as a callback.  
  
## Application Domains and Calling Conventions  
 Although it is possible for pure MSIL assemblies use unmanaged functionality, functions and static data are handled differently. In pure assemblies, functions are implemented with the [__clrcall](../Topic/__clrcall.md) calling convention, and static data is stored per-application domain. This differs from the default for unmanaged and mixed assemblies, which use the [__cdecl](../vs140/__cdecl.md) calling convention for functions and store static data on a per-process basis.  
  
 Within the context of pure MSIL (and verifiable code compiled with /clr:safe) these defaults are transparent, as [__clrcall](../Topic/__clrcall.md) is the default calling convention of the CLR, and application domains are the native scope for static and global data in .NET applications. However, when interfacing with unmanaged or mixed components, the differing treatment of functions and global data can cause problems.  
  
 For example, if a pure MSIL component is to call functions in an unmanaged or mixed DLL, a header file for the DLL will be used to compile the pure assembly. However, unless the calling convention for each function in the header is indicated explicitly, they will all be assumed to be [__clrcall](../Topic/__clrcall.md). This will later cause runtime failures, as these functions are likely implemented with the [__cdecl](../vs140/__cdecl.md) convention. The functions in the unmanaged header file can be explicitly marked as [__cdecl](../vs140/__cdecl.md), or the entire DLL source code must be recompiled under **/clr:pure**.  
  
 Similarly, function pointers are assumed to point to [__clrcall](../Topic/__clrcall.md) functions under **/clr:pure** compilation. These too must be explicitly annotated with the correct calling convention.  
  
 For more information, see [Application Domains and Visual C++](../vs140/Application-Domains-and-Visual-C--.md).  
  
## Linking Limitations  
 The Visual C++ linker will not attempt to link mixed and pure OBJ files, as the storage scope and calling conventions are different.  
  
## See Also  
 [Pure and Verifiable Code](../vs140/Pure-and-Verifiable-Code--C---CLI-.md)