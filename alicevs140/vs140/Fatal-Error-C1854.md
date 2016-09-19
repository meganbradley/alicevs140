---
title: "Fatal Error C1854"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 8c21a9cc-1737-475c-9e57-8725cd8937c1
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1854
cannot overwrite information formed during creation of the precompiled header in object file: 'filename'  
  
 You specified the **/Yu** (use precompiled header) option after specifying the **/Yc** (create precompiled header) option for the same file. Certain declarations (such as declarations including `__declspec` `dllexport`) make this invalid.