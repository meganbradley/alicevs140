---
title: "Compiler Warning (level 1) C4627"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8840f3e6-b496-423a-8635-eb55d5f854a2
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4627
'<identifier\>': skipped when looking for precompiled header use  
  
 While searching for the location where a precompiled header is used, the compiler encountered an `#include` directive for the *<identifier\>* include file. The compiler ignores the `#include` directive, but issues warning **C4627** if the precompiled header does not already contain the *<identifier\>* include file.  
  
## See Also  
 [Creating Precompiled Header Files](../vs140/Creating-Precompiled-Header-Files.md)