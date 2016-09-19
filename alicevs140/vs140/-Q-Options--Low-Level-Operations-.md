---
title: "-Q Options (Low-Level Operations)"
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
H1: /Q Options (Low-Level Operations)
ms.assetid: 9fa738b9-630a-4bde-bc87-bdfa30552be4
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Q Options (Low-Level Operations)
You can use the **/Q** compiler options to perform the following low-level compiler operations:  
  
-   [/Qfast_transcendentals (Force Fast Transcendentals)](../vs140/-Qfast_transcendentals--Force-Fast-Transcendentals-.md): Generates fast transcendentals.  
  
-   [/QIfist (Suppress _ftol)](../Topic/-QIfist%20\(Suppress%20_ftol\).md): Suppresses `_ftol` when a conversion from a floating-point type to an integer type is required (x86 only).  
  
-   [/Qimprecise_fwaits (Remove fwaits Inside try Blocks)](../vs140/-Qimprecise_fwaits--Remove-fwaits-Inside-Try-Blocks-.md): Removes `fwait` commands inside `try` blocks.  
  
-   [/Qpar (Auto-Parallelizer)](../Topic/-Qpar%20\(Auto-Parallelizer\).md): Enables automatic parallelization of loops that are marked with the [#pragma loop()](../vs140/loop.md) directive.  
  
-   [/Qpar-report (Auto-Parallelizer)](../vs140/-Qpar-report--Auto-Parallelizer-Reporting-Level-.md): Enables reporting levels for automatic parallelization.  
  
-   [/Qsafe_fp_loads](../vs140/-Qsafe_fp_loads.md): Suppresses optimizations for floating-point register loads and for moves between memory and MMX registers.  
  
-   [/Qvec-report (Auto-Vectorizer)](../Topic/-Qvec-report%20\(Auto-Vectorizer%20Reporting%20Level\).md): Enables reporting levels for automatic vectorization.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)