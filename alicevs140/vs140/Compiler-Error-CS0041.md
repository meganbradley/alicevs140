---
title: "Compiler Error CS0041"
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
ms.assetid: 80dbfe00-8cdb-4275-9574-8a215c7139d6
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0041
The fully qualified name for 'type' is too long for debug information. Compile without '/debug' option.  
  
 This error can occur when using the [/debug](../Topic/-debug%20\(C%23%20Compiler%20Options\).md) compiler option. If you encounter this error, try to delete the PDB files in the bin directory and recompiling. If you are still encountering this error, you may have to repair or reinstall [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].