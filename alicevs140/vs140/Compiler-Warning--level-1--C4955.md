---
title: "Compiler Warning (level 1) C4955"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a26ebcb3-9be1-49c8-ac94-c285aeec8e76
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4955
'import2' : import ignored; already imported from 'import1'  
  
 The compiler found two [#using](../vs140/#using-Directive--C---.md) statements that reference the same assembly.  
  
 To resolve this warning, delete one `#using` statement.