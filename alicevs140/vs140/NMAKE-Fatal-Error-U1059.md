---
title: "NMAKE Fatal Error U1059"
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
ms.assetid: b21d9198-9c63-40d0-b589-80e17294ce24
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Fatal Error U1059
syntax error : '}' missing in dependent  
  
 A search path for a dependent was incorrectly specified. Either a space existed in the path or the closing brace (**}**) was omitted.  
  
 The syntax for a directory specification for a dependent is  
  
 **{**   
 ***directories* }dependent**  
  
 where `directories` specifies one or more paths, each separated by a semicolon (**;**). No spaces are allowed.  
  
 If part or all of a search path is replaced by a macro, make sure no spaces exist in the macro expansion.