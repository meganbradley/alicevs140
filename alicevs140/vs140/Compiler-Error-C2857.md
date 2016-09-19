---
title: "Compiler Error C2857"
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
ms.assetid: b57302bd-58ec-45ae-992a-1e282d5eeccc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2857
'#include' statement specified with the /Ycfilename command-line option was not found in the source file  
  
 The [/Yc](../vs140/-Yc--Create-Precompiled-Header-File-.md) option specifies the name of an include file that is not included in the source file being compiled.  
  
 This error can be caused by a `#include` statement in a conditional compilation block that is not compiled.