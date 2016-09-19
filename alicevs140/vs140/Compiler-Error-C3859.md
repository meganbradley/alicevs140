---
title: "Compiler Error C3859"
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
ms.topic: error-reference
ms.assetid: 40e93b25-4393-4467-90de-035434a665c7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3859
virtual memory range for PCH exceeded; please recompile with a command line option of '-Zmvalue' or greater  
  
 Your precompiled header is too small for the amount of data the compiler is trying to put in it. Use the **/Zm** compiler flag to specify a larger value for the precompiled header file. For more information, see [/Zm (Specify Precompiled Header Memory Allocation Limit)](../Topic/-Zm%20\(Specify%20Precompiled%20Header%20Memory%20Allocation%20Limit\).md).