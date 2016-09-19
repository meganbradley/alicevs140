---
title: "Compiler Error C2567"
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
ms.assetid: 9c140ac9-7059-47e6-9ba1-e7939c8c0dc3
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2567
unable to open metadata in 'file', file may have been deleted or moved  
  
 A metadata file that was referenced in source (with `#using`) was not found in the same directory by the compiler back end process as it was by the compiler front end process. See [The #using Directive](../vs140/#using-Directive--C---.md) for more information.  
  
 C2567 could be caused if you compile with **/c** on one machine and then attempt a link-time code generation on another machine. For more information, see [/LTCG (Link-time Code Generation)](../vs140/-LTCG--Link-time-Code-Generation-.md)).  
  
 It might also indicate that your computer had no  more memory.  
  
 To correct this error, make sure that the metadata file is in the same directory location for all phases of the build process.