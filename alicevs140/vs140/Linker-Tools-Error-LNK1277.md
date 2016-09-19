---
title: "Linker Tools Error LNK1277"
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
ms.assetid: afca3de0-50cc-4140-af7a-13493a170835
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1277
object record not found in pgd (filename)  
  
 When using [/LTCG:PGOPTIMZE](../vs140/-LTCG--Link-time-Code-Generation-.md), the path of one of the input .lib, def, or .obj files was different from the path on which they were found during /LTCG:PGINSTRUMENT. This may be explained by a change in the LIB environment variable after /LTCG:PGINSTRUMENT. The full path to the input files is stored in the .pgd file.  
  
 /LTCG:PGOPTIMIZE requires that the inputs be identical to the /LTCG:PGINSTRUMENT phase.  
  
 To resolve this warning, do one of the following:  
  
-   Run /LTCG:PGINSTRUMENT, redo all test runs, and run /LTCG:PGOPTIMIZE.  
  
-   Change the LIB environment variable to what it was when you ran /LTCG:PGINSTRUMENT.  
  
 It is not recommended that you work around LNK1277 by using /LTCG:PGUPDATE.