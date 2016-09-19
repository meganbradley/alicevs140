---
title: "Compiler Error CS1906"
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
ms.assetid: 1a6abf5c-f673-4256-93ac-313dce50acc0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1906
Invalid option 'option'; Resource visibility must be either 'public' or 'private'  
  
 This error indicates an invalid [/resource (Embed Resource File to Output)](../Topic/-resource%20\(C%23%20Compiler%20Options\).md) or [/linkresource (Link to .NET Framework Resource)](../Topic/-linkresource%20\(C%23%20Compiler%20Options\).md) command line option. Check the syntax of the **/resource** or **/linkresource** command line option, and make sure that the accessibility modifier used is either **public** or `private`.