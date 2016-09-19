---
title: "Fatal Error C1852"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fa011004-b8d6-46f1-ba80-4785e4ce137f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1852
'filename' is not a valid precompiled header file  
  
 The file is not a precompiled header.  
  
### To fix by checking the following possible causes  
  
1.  Invalid file specified with **/Yu** or **#pragma hdrstop**.  
  
2.  The compiler assumes a file extension of .pch if you do not specify otherwise.