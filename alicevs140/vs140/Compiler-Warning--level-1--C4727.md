---
title: "Compiler Warning (level 1) C4727"
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
ms.assetid: 991b0087-3a50-40f5-9cdb-cdc367cd472c
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4727
"PCH named pch_file with same timestamp found in obj_file_1 and obj_file_2.  Using first PCH.  
  
 C4727 occurs when compiling multiple compilands with **/Yc**, and where the compiler was able to mark all .obj files with the same .pch timestamp.  
  
 To resolve, compile one source file with **/Yc /c** (creates pch), and the others compile separately with **/Yu /c** (uses pch), then link them together.  
  
 So, if you did the following and generates C4727:  
  
 **cl /clr /GL a.cpp b.cpp c.cpp /Ycstdafx.h**  
  
 You would do the following instead:  
  
 **cl /clr /GL a.cpp /Ycstdafx.h /c**  
  
 **cl /clr /GL b.cpp c.cpp /Yustdafx.h /link a.obj**  
  
 For more information, see  
  
-   [/Yc (Create Precompiled Header File)](../vs140/-Yc--Create-Precompiled-Header-File-.md)  
  
-   [/Yu (Use Precompiled Header File)](../vs140/-Yu--Use-Precompiled-Header-File-.md)