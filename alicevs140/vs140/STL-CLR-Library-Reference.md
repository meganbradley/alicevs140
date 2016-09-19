---
title: "STL-CLR Library Reference"
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
ms.topic: reference
H1: STL/CLR Library Reference
ms.assetid: a9d9ca00-7bf2-48c1-b205-3ae6f8c25f82
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# STL-CLR Library Reference
The STL/CLR Library is a packaging of the Standard Template Library (STL), a subset of the Standard C++ Library, for use with C++ and the .NET Framework common language runtime (CLR). With STL/CLR, you can use all the containers, iterators, and algorithms of STL in a managed environment.  
  
 To use STL/CLR:  
  
-   Include headers from the **cliext** include subdirectory instead of the usual Standard C++ Library equivalents.  
  
-   Qualify library names with `cliext::` instead of `std::`.  
  
 STL/CLR exposes the generic types and interfaces that it uses in cross-assembly scenarios in the .NET assembly **Microsoft.VisualC.STLCLR.dll**. This DLL is included in .NET Framework 3.5. If you redistribute an application that uses STL/CLR, you will need to include the .NET Framework 3.5, as well as any other Visual C++ libraries that your project uses, in the dependencies section of your setup project.  
  
## In This Section  
 [cliext Namespace](../vs140/cliext-Namespace.md)  
 Discusses the namespace that contains all the types of the STL/CLR Library.  
  
 [STL/CLR Containers](../vs140/STL-CLR-Containers.md)  
 Provides an overview of the containers that are found in the Standard C++ Library, including requirements for container elements, types of elements that can be inserted, and ownership issues.  
  
 [Requirements for STL and STL/CLR Container Elements](../vs140/Requirements-for-STL-CLR-Container-Elements.md)  
 Describes minimum requirements for all reference types that are inserted into STL containers.  
  
 [How to: Convert from a .NET Collection to a STL/CLR Container](../vs140/How-to--Convert-from-a-.NET-Collection-to-a-STL-CLR-Container.md)  
 Describes how to convert a .NET collection to an STL/CLR container.  
  
 [How to: Convert from a STL/CLR Container to a .NET Collection](../Topic/How%20to:%20Convert%20from%20a%20STL-CLR%20Container%20to%20a%20.NET%20Collection.md)  
 Describes how to convert an STL/CLR container to a .NET collection.  
  
 [How to: Expose an STL/CLR Container from an Assembly](../vs140/How-to--Expose-an-STL-CLR-Container-from-an-Assembly.md)  
 Shows how to display the elements of several STL/CLR containers written in a C++ assembly.  
  
 In addition, this section also describes the following components of STL/CLR:  
  
|||  
|-|-|  
|[adapter (STL/CLR)](../vs140/adapter--STL-CLR-.md)|[algorithm (STL/CLR)](../vs140/algorithm--STL-CLR-.md)|  
|[deque (STL/CLR)](../Topic/deque%20\(STL-CLR\).md)|[for each, in](../Topic/for%20each,%20in.md)|  
|[functional (STL/CLR)](../vs140/functional--STL-CLR-.md)|[hash_map (STL/CLR)](../Topic/hash_map%20\(STL-CLR\).md)|  
|[hash_multimap (STL/CLR)](../Topic/hash_multimap%20\(STL-CLR\).md)|[hash_multiset (STL/CLR)](../Topic/hash_multiset%20\(STL-CLR\).md)|  
|[hash_set (STL/CLR)](../Topic/hash_set%20\(STL-CLR\).md)|[list (STL/CLR)](../Topic/list%20\(STL-CLR\).md)|  
|[map (STL/CLR)](../Topic/map%20\(STL-CLR\).md)|[multimap (STL/CLR)](../Topic/multimap%20\(STL-CLR\).md)|  
|[multiset (STL/CLR)](../Topic/multiset%20\(STL-CLR\).md)|[numeric (STL/CLR)](../vs140/numeric--STL-CLR-.md)|  
|[priority_queue (STL/CLR)](../Topic/priority_queue%20\(STL-CLR\).md)|[queue (STL/CLR)](../Topic/queue%20\(STL-CLR\).md)|  
|[set (STL/CLR)](../Topic/set%20\(STL-CLR\).md)|[stack (STL/CLR)](../Topic/stack%20\(STL-CLR\).md)|  
|[utility (STL/CLR)](../vs140/utility--STL-CLR-.md)|[vector (STL/CLR)](../Topic/vector%20\(STL-CLR\).md)|  
  
## See Also  
 [Standard C++ Library Reference](../vs140/C---Standard-Library-Reference.md)