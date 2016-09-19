---
title: "-LN (Create MSIL Module)"
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
H1: /LN (Create MSIL Module)
ms.assetid: 4f38f4f4-3176-4caf-8200-5c7585dc1ed3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -LN (Create MSIL Module)
Specifies that an assembly manifest should not be inserted into the output file.  
  
## Syntax  
  
```  
/LN  
```  
  
## Remarks  
 By default, **/LN** is not in effect (an assembly manifest is inserted into the output file).  
  
 When **/LN** is used, one of the [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) options must also be used.  
  
 A managed program that does not have an assembly metadata in the manifest is called a module. If you compile with [/c (Compile Without Linking)](../Topic/-c%20\(Compile%20Without%20Linking\).md) and **/LN**, specify [/NOASSEMBLY (Create a MSIL Module)](../Topic/-NOASSEMBLY%20\(Create%20a%20MSIL%20Module\).md) in the linker phase to create the output file.  
  
 You may want to create modules if you want to take a component-based approach to building assemblies.  That is, you can author types and compile them into modules.  Then, you can generate an assembly from one or more modules.  For more information on creating assemblies from modules, see [.netmodule Files as Linker Input](../vs140/.netmodule-Files-as-Linker-Input.md) or [Assembly Linker (Al.exe)](assetId:///b5382965-0053-47cf-b92f-862860275a01).  
  
 The default file extension for a module is .netmodule.  
  
 In [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] releases before Visual C++ 2005, a module was created with **/clr:noAssembly**.  
  
 The Visual C++ linker accepts .netmodule files as input and the output file produced by the linker will be an assembly or .netmodule with no run-time dependence on any of the .netmodules that were input to the linker.  For more information, see [.netmodule Files as Linker Input](../vs140/.netmodule-Files-as-Linker-Input.md).  
  
### To set this compiler option in the Visual Studio development environment  
  
-   Specify [/NOASSEMBLY (Create a MSIL Module)](../Topic/-NOASSEMBLY%20\(Create%20a%20MSIL%20Module\).md) in the linker phase to create the output file.  
  
### To set this compiler option programmatically  
  
-   This compiler option cannot be changed programmatically.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)