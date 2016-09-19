---
title: "Building an Attributed Program"
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
ms.assetid: 04997b5f-bf2c-46ec-b868-c4adebbef5f4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Building an Attributed Program
After you put Visual C++ attributes into your source code, you may want the Visual C++ compiler to produce a type library and .idl file for you. The following linker options help you build .tlb and .idl files:  
  
-   [/IDLOUT](../vs140/-IDLOUT--Name-MIDL-Output-Files-.md)  
  
-   [/IGNOREIDL](../Topic/-IGNOREIDL%20\(Don't%20Process%20Attributes%20into%20MIDL\).md)  
  
-   [/MIDL](../vs140/-MIDL--Specify-MIDL-Command-Line-Options-.md)  
  
-   [/TLBOUT](../vs140/-TLBOUT--Name-.TLB-File-.md)  
  
 Some projects contain multiple independent .idl files. These are used to produce two or more .tlb files and optionally bind them into the resource block. This scenario is not currently supported in Visual C++.  
  
 In addition, the Visual C++ linker will output all IDL-related attribute information to a single MIDL file. There will be no way to generate two type libraries from a single project.  
  
## See Also  
 [Concepts](../vs140/Attributed-Programming-Concepts.md)