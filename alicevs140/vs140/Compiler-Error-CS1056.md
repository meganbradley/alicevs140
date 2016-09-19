---
title: "Compiler Error CS1056"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bf66d164-ab5b-4181-b93e-a1d29620b4d2
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1056
Unexpected character 'character'  
  
 The C# compiler encountered an unexpected character, and is unable to identify the token currently being processed. For example, if the compiler encounters a Euro-character in the middle of processing an identifier, it will be unable to classify the identifier, since a Euro-character would only be valid inside a string, and the compiler knows it is not processing a string.