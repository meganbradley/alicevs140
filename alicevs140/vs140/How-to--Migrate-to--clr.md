---
title: "How to: Migrate to -clr"
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
ms.topic: get-started-article
H1: How to: Migrate to /clr
ms.assetid: c9290b8b-436a-4510-8b56-eae51f4a9afc
caps.latest.revision: 39
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Migrate to -clr
This topic discusses issues that arise when compiling native code with **/clr** (see [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) for more information). **/clr** allows Visual C++ modules to invoke and be invoked from .NET assemblies while retaining compatibility with unmanaged modules. See [Mixed Assemblies](../vs140/Mixed--Native-and-Managed--Assemblies.md) and [Native and .NET Interoperability](../vs140/Native-and-.NET-Interoperability.md) for more information on the advantages of compiling with **/clr**.  
  
## Known Issues Compiling Library Projects with /clr  
 Visual Studio contains some known issues when compiling library projects with **/clr**:  
  
-   Your code may query types at runtime with [CRuntimeClass::FromName](../vs140/CRuntimeClass--FromName.md). However, if a type is in an MSIL .dll (compiled with **/clr**), the call to [CRuntimeClass::FromName](../vs140/CRuntimeClass--FromName.md) may fail if it occurs before the static constructors run in the managed .dll (you will not see this problem if the FromName call happens after code has executed in the managed .dll). To work around this problem, you can force the construction of the managed static constructor by defining a function in the managed .dll, exporting it, and invoking it from the native MFC application. For example:  
  
    ```  
    // Extension DLL Header file:  
    __declspec( dllexport ) void EnsureManagedInitialization () {  
       // managed code that won't be optimized away  
       System::GC::KeepAlive(System::Int32::MaxValue);  
    }  
    ```  
  
## Compile with Visual C++  
 Before using **/clr** on any module in your project, first compile and link your native project with Visual Studio 2010.  
  
 The following steps, followed in order, provide the easiest path to a **/clr** compilation. It is important to compile and run your project after each of these steps.  
  
### Versions Prior to Visual C++ 2003  
 If you are upgrading to Visual Studio 2010 from a version prior to Visual C++ 2003, you may see compiler errors related to the enhanced C++ standard conformance in Visual C++ 2003  
  
### Upgrading from Visual C++ 2003  
 Projects previous built with Visual C++ 2003 should also first be compiled without **/clr** as Visual Studio now has increased ANSI/ISO compliance and some breaking changes. The change that is likely to require the most attention is [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md). Code that uses the CRT is very likely to produce deprecation warnings. These warnings can be suppressed, but migrating to the new [Security-Enhanced Versions of CRT Functions](../vs140/Security-Enhanced-Versions-of-CRT-Functions.md) is preferred, as they provide better security and may reveal security issues in your code.  
  
### Upgrading from Managed Extensions for C++  
 Projects built with Visual C++ .NET or Visual C++ 2003 that used Managed Extensions for C++ will require at least one change to project settings, as these extensions are now deprecated. As a result, code written with Managed Extensions for C++ won't compile under **/clr**. Use **/clr:oldSyntax** instead.  
  
## Convert C Code to C++  
 Although Visual Studio will compile C files, it is necessary to convert them to C++ for a **/clr** compilation. The actual filename doesn't have to be changed; you can use **/Tp** (see [/Tc, /Tp, /TC, /TP (Specify Source File Type)](../vs140/-Tc---Tp---TC---TP--Specify-Source-File-Type-.md).) Note that although C++ source code files are required for **/clr**, it is not necessary to re-factor your code to use object-oriented paradigms.  
  
 C code is very likely to require changes when compiled as a C++ file. The C++ type-safety rules are strict, so type conversions must be made explicit with casts. For example, malloc returns a void pointer, but can be assigned to a pointer to any type in C with a cast:  
  
```  
int* a = malloc(sizeof(int));   // C code  
int* b = (int*)malloc(sizeof(int));   // C++ equivalent  
```  
  
 Function pointers are also strictly type-safe in C++, so the following C code requires modification. In C++ it's best to create a `typedef` that defines the function pointer type, and then use that type to cast function pointers:  
  
```  
NewFunc1 = GetProcAddress( hLib, "Func1" );   // C code  
typedef int(*MYPROC)(int);   // C++ equivalent  
NewFunc2 = (MYPROC)GetProcAddress( hLib, "Func2" );  
```  
  
 C++ also requires that functions either be prototyped or fully defined before they can be referenced or invoked.  
  
 Identifiers used in C code that happen to be keywords in C++ (such as `virtual`, `new`, `delete`, `bool`, `true`, `false`, etc.) must be renamed. This can generally be done with simple search-and-replace operations.  
  
 Finally, whereas C-style COM calls require explicit use of the v-table and `this` pointer, C++ does not:  
  
```  
COMObj1->lpVtbl->Method(COMObj, args);  // C code  
COMObj2->Method(args);  // C++ equivalent  
```  
  
## Reconfigure Project Settings  
 After your project compiles and runs in Visual Studio 2010 you should create new project configurations for **/clr** rather than modifying the default configurations. **/clr** is incompatible with some compiler options and creating separate configurations lets you build your project as native or managed. When **/clr** is selected in the property pages dialog box, project settings not compatible with **/clr** are disabled (and disabled options are not automatically restored if **/clr** is subsequently unselected).  
  
### Create New Project Configurations  
 You can use **Copy Settings From** option in the [New Project Configuration Dialog Box](assetId:///cca616dc-05a6-4fe3-bdc1-40c72a66f2be) to create a project configuration based on your existing project settings. Do this once for the Debug configuration and once for Release configuration. Subsequent changes can then be applied to the **/clr** -specific configurations only, leaving the original project configurations intact.  
  
 Projects that use custom build rules may require extra attention.  
  
 This step has different implications for projects that use makefiles. In this case a separate build-target can be configured, or version specific to **/clr** compilation can be created from a copy of the original.  
  
### Change Project Settings  
 **/clr** can be selected in the development environment by following the instructions in [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md). As mentioned previously, this step will automatically disable conflicting project settings.  
  
> [!NOTE]
>  When upgrading a managed library or web service project from Visual C++ 2003, the **/Zl** compiler option will added to the **Command Line** property page. This will cause LNK2001. Remove **/Zl** from the **Command Line** property page to resolve. See [/Zl (Omit Default Library Name)](../vs140/-Zl--Omit-Default-Library-Name-.md) and [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md) for more information. Or, add msvcrt.lib and msvcmrt.lib to the linker's **Additional Dependencies** property.  
  
 For projects built with makefiles, incompatible compiler options must be disabled manually once **/clr** is added. See /[/clr Restrictions](../Topic/-clr%20Restrictions.md) for information on compiler options that are not compatible with **/clr**.  
  
### Precompiled Headers  
 Precompiled headers are supported under **/clr**. However, if you only compile some of your CPP files with **/clr** (compiling the rest as native) some changes will be required because precompiled headers generated with **/clr** are not compatible with those generated without **/clr**. This incompatibility is due to the fact that **/clr** generates and requires metadata. Modules compiled **/clr** can therefore not use precompiled headers that don't include metadata, and non **/clr** modules can't use precompiled header files that do contain meta data.  
  
 The easiest way to compile a project where some modules are compiled **/clr** is to disable precompiled headers entirely. (In the project Property Pages dialog, open the C/C++ node, and select Precompiled Headers. Then change the Create/Use Precompiled Headers property to "Not Using Precompiled Headers".)  
  
 However, particularly for large projects, precompiled headers provide much better compilation speed, so disabling this feature is not desirable. In this case it's best to configure the **/clr** and non **/clr** files to use separate precompiled headers. This can be done in one step by multi-selecting the modules to be compiled **/clr** using the Solution Explorer, right-clicking on the group, and selecting Properties. Then change both the Create/Use PCH Through File and Precompiled Header File properties to use a different header file name and PCH file respectively.  
  
## Fixing Errors  
 Compiling with **/clr** may result in compiler, linker or runtime errors. This section discusses the most common problems.  
  
### Metadata Merge  
 Differing versions of data types can cause the linker to fail because the metadata generated for the two types doesn't match. (This is usually caused when members of a type are conditionally defined, but the conditions are not the same for all CPP files that use the type.) In this case the linker fails, reporting only the symbol name and the name of the second OBJ file where the type was defined. It is often useful to rotate the order that OBJ files are sent to the linker to discover the location of the other version of the data type.  
  
### Loader Lock Deadlock  
 In Visual C++ .NET and Visual C++ 2003, initialization under **/clr** was susceptible to non-deterministic deadlock. This issue is known as "loader lock deadlock". In Visual Studio 2010, this deadlock is easier to avoid, it is detected and reported at runtime, and is no longer non-deterministic. Encountering the loader lock problem is still possible, but now it's much easier to avoid and fix. See [Initialization of Mixed Assemblies](../vs140/Initialization-of-Mixed-Assemblies.md) for detailed background, guidance, and solutions.  
  
### Data Exports  
 Exporting DLL data is error-prone, and not recommended. This is because the data section of a DLL is not guaranteed to be initialized until some managed portion of the DLL has been executed. Reference metadata with [The #using Directive](../vs140/#using-Directive--C---.md).  
  
### Type Visibility  
 Native types are now private by default. In Visual C++ .NET 2002 and Visual C++ 2003, native types were public by default. This can result in a native type not being visible outside the DLL. Resolve this error by adding `public` to these types. See [Type and Member Visibility](../vs140/Type-and-Member-Visibility.md) for more information.  
  
### Floating Point and Alignment Issues  
 `__controlfp` is not supported on the common language runtime (see [_control87, _controlfp, \__control87_2](../vs140/_control87--_controlfp--__control87_2.md) for more information). The CLR will also not respect [align (C++)](../vs140/align--C---.md).  
  
### COM Initialization  
 The Common Language Runtime initializes COM automatically when a module is initialized (when COM is initialized automatically it’s done so as MTA). As a result, explicitly initializing COM yields return codes indicating that COM is already initialized. Attempting to explicitly initialize COM with one threading model when the CLR has already initialized COM to another threading model can cause your application to fail.  
  
 The common language runtime starts COM as MTA by default; use [/CLRTHREADATTRIBUTE (Set CLR Thread Attribute)](../Topic/-CLRTHREADATTRIBUTE%20\(Set%20CLR%20Thread%20Attribute\).md) to modify this.  
  
### Performance Issues  
 You may see decreased performance when native C++ methods generated to MSIL are called indirectly (virtual function calls or using function pointers). To learn more about this, see [Double Thunking](../vs140/Double-Thunking--C---.md).  
  
 When moving from native to MSIL, you will notice an increase in the size of your working set. This is because the common language runtime provides many features to ensure that programs run correctly. If your **/clr** application is not running correctly, you may want to enable C4793 (off by default), see [Compiler Warning (level 1 and 3) C4793](../vs140/Compiler-Warning--level-1-and-3--C4793.md) for more information.  
  
### Program Crashes on Shutdown  
 In some cases, the CLR can shutdown before your managed code is finished running. Using `std::set_terminate` and `SIGTERM` can cause this. See [signal Constants](../vs140/signal-Constants.md) and [set_terminate (<exception\>)](../vs140/set_terminate---exception--.md) for more information.  
  
## Using New Visual C++ Features  
 After your application compiles, links, and runs, you can begin using .NET features in any module compiled with **/clr**. For more information, see [New C++ Language Features](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md).  
  
 If you used Managed Extensions for C++, you can convert your code to use the new syntax. For a summary of syntactical differences, see the [(NOTINBUILD)Managed Extensions for C++ Syntax Upgrade Checklist](assetId:///edbded88-7ef3-4757-bd9d-b8f48ac2aada). For details on converting Managed Extensions for C++, see [C++/CLI Migration Primer](../vs140/C---CLI-Migration-Primer.md).  
  
 For information on .NET programming in Visual C++ see:  
  
-   [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)  
  
-   [Native and .NET Interoperability](../vs140/Native-and-.NET-Interoperability.md)  
  
-   [New C++ Language Features](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)  
  
## See Also  
 [Mixed Assemblies](../vs140/Mixed--Native-and-Managed--Assemblies.md)