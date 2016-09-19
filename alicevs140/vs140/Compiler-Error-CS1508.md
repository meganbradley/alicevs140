---
title: "Compiler Error CS1508"
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
ms.assetid: 979bc615-58ce-49f8-ba73-e6cf57c56418
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1508
Resource identifier 'identifier' has already been used in this assembly  
  
 In a compilation, the same identifier (***identifier***) was passed to two or more [/resource](../Topic/-resource%20\(C%23%20Compiler%20Options\).md) or [/linkresource](../Topic/-linkresource%20\(C%23%20Compiler%20Options\).md) compiler options.  
  
 For example, the following options would generate CS1508:  
  
```  
/resource:anyfile.bmp,DuplicatIdent /linkresource:a.bmp,DuplicatIdent  
```