---
title: "Edit and Continue Not Supported for F#"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40ec77bb-07e3-4b58-9254-ae015009441c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Edit and Continue Not Supported for F#
Edit and Continue is not supported when you debug F# code. Edits to F# code are possible during a debugging session but should be avoided. Code changes are not applied during the debugging session. Therefore, any edits made to F# code while you debug will result in source code that does not match the code being debugged.