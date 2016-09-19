---
title: "-KEYCONTAINER (Specify a Key Container to Sign an Assembly)"
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
H1: /KEYCONTAINER (Specify a Key Container to Sign an Assembly)
ms.assetid: 94882d12-b77a-49c7-96d0-18a31aee001e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -KEYCONTAINER (Specify a Key Container to Sign an Assembly)
```  
/KEYCONTAINER:name  
```  
  
## Remarks  
 where,  
  
 *name*  
 Container that contains the key. Place the string in double quotation marks (" ") if it contains a space.  
  
## Remarks  
 The linker creates a signed assembly by inserting a public key into the assembly manifest and signing the final assembly with the private key. To generate a key file, type [sn -k](assetId:///c1d2b532-1b8e-4c7a-8ac5-53b801135ec6) `file` at the command line. **sn -i** installs the key pair into a container.  
  
 If you compile with [/LN](../vs140/-LN--Create-MSIL-Module-.md), the name of the key file is held in the module and incorporated into the assembly that is created when you compile an assembly that includes an explicit reference to the module, via [#using](../vs140/#using-Directive--C---.md), or when linking with [/ASSEMBLYMODULE](../Topic/-ASSEMBLYMODULE%20\(Add%20a%20MSIL%20Module%20to%20the%20Assembly\).md).  
  
 You can also pass your encryption information to the compiler with [/KEYFILE](../Topic/-KEYFILE%20\(Specify%20Key%20or%20Key%20Pair%20to%20Sign%20an%20Assembly\).md). Use [/DELAYSIGN](../Topic/-DELAYSIGN%20\(Partially%20Sign%20an%20Assembly\).md) if you want a partially signed assembly. See [Strong Name Assemblies (Assembly Signing)](../Topic/Strong%20Name%20Assemblies%20\(Assembly%20Signing\)%20\(C++-CLI\).md) for more information on signing an assembly.  
  
 Other linker options that affect assembly generation are:  
  
-   [/ASSEMBLYDEBUG](../Topic/-ASSEMBLYDEBUG%20\(Add%20DebuggableAttribute\).md)  
  
-   [/ASSEMBLYLINKRESOURCE](../Topic/-ASSEMBLYLINKRESOURCE%20\(Link%20to%20.NET%20Framework%20Resource\).md)  
  
-   [/ASSEMBLYMODULE](../Topic/-ASSEMBLYMODULE%20\(Add%20a%20MSIL%20Module%20to%20the%20Assembly\).md)  
  
-   [/ASSEMBLYRESOURCE](../Topic/-ASSEMBLYRESOURCE%20\(Embed%20a%20Managed%20Resource\).md)  
  
-   [/NOASSEMBLY](../Topic/-NOASSEMBLY%20\(Create%20a%20MSIL%20Module\).md)  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Command Line** property page.  
  
4.  Type the option into the **Additional Options** box.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)