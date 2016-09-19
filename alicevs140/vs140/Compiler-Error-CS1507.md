---
title: "Compiler Error CS1507"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e1be3aba-81dc-4f65-87a4-d3f90b82dc7d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1507
Cannot link resource file 'file' when building a module  
  
 [/linkresource](../Topic/-linkresource%20\(C%23%20Compiler%20Options\).md) was used in the same compilation with [/target:module](../vs140/-target-module--C#-Compiler-Options-.md), which is not allowed. For example, the following options would generate CS1507:  
  
```  
csc /linkresource:rf.resource /target:module in.cs  
```  
  
 Embeding resourrces ([/resource](../Topic/-resource%20\(C%23%20Compiler%20Options\).md)), however, is allowed.