---
title: "Manifest Generation at the Command Line"
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
ms.assetid: fc2ff255-82b1-4c44-af76-8405c5850292
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Manifest Generation at the Command Line
When building C/C++ applications from the command line using nmake or similar tools, the manifest is generated after the linker has processed all object files and built the final binary. The linker collects assembly information stored in the object files and combines this information into a final manifest file. By default the linker will generate a file named <binary_name>.<extension\>.manifest to describe the final binary. The linker does not embed a manifest file inside the binary and can only generate a manifest as an external file. There are several ways to embed a manifest inside the final binary, such as using the [Manifest Tool (mt.exe)](http://msdn.microsoft.com/library/aa375649) or compiling the manifest into a resource file. It is important to keep in mind that specific rules have to be followed when embedding a manifest inside the final binary to enable such features as incremental linking, signing, and edit and continue. These and other options are discussed in [Embedding a Manifest Inside a C/C++ Application](../vs140/How-to--Embed-a-Manifest-Inside-a-C-C---Application.md) when building on the command line.  
  
## See Also  
 [Manifests](http://msdn.microsoft.com/library/aa375365)   
 [/INCREMENTAL (Link Incrementally)](../Topic/-INCREMENTAL%20\(Link%20Incrementally\).md)   
 [Strong Name Assemblies (Assembly Signing)](../Topic/Strong%20Name%20Assemblies%20\(Assembly%20Signing\)%20\(C++-CLI\).md)   
 [Edit and Continue](../vs140/Edit-and-Continue.md)   
 [Understanding Manifest Generation for C/C++ Programs](../vs140/Understanding-Manifest-Generation-for-C-C---Programs.md)