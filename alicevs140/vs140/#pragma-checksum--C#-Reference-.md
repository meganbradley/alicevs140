---
title: "#pragma checksum (C# Reference)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3673e4ca-6098-4ec1-890f-8fceb2a794a2
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #pragma checksum (C# Reference)
Generates checksums for source files to aid with debugging [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] pages.  
  
## Syntax  
  
```  
#pragma checksum "filename" "{guid}" "checksum bytes"  
```  
  
#### Parameters  
 `"filename"`  
 The name of the file that requires monitoring for changes or updates.  
  
 `"{guid}"`  
 The Globally Unique Identifier (GUID) for the file.  
  
 `"checksum_bytes"`  
 The string of hexadecimal digits representing the bytes of the checksum. Must be an even number of hexadecimal digits. An odd number of digits results in a compile-time warning, and the directive are  ignored.  
  
## Remarks  
 The Visual Studio debugger uses a checksum to make sure  that it always finds the right source. The compiler computes the checksum for a source file, and then emits the output to the program database (PDB) file. The debugger then uses the PDB to compare against the checksum that it computes for the source file.  
  
 This solution does not work for [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] projects, because the computed checksum is for the generated source file, rather than the .aspx file. To address this problem, `#pragma checksum` provides checksum support for [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] pages.  
  
 When you create an [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] project in [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)], the generated source file contains a checksum for the .aspx file, from which the source is generated. The compiler then writes this information into the PDB file.  
  
 If the compiler encounters no `#pragma checksum` directive in the file, it computes the checksum and writes the value to the PDB file.  
  
## Example  
  
```  
class TestClass  
{  
    static int Main()  
    {  
        #pragma checksum "file.cs" "{3673e4ca-6098-4ec1-890f-8fceb2a794a2}" "{012345678AB}" // New checksum  
    }  
}  
```  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)