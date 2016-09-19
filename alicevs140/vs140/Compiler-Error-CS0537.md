---
title: "Compiler Error CS0537"
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
ms.assetid: 6c832a5f-47dc-4f60-aed8-69ac328af44b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0537
The class System.Object cannot have a base class or implement an interface  
  
 CS0537 occurs when rebuilding the <xref:System?qualifyHint=False> class libraries, and where <xref:System.Object?qualifyHint=False> derives from another class. You are very unlikely to encounter this error. If you do, do not derive <xref:System.Object?qualifyHint=False> from a class or interface: it is the root of the entire .NET Framework class hierarchy, and as such, does not derive from anything else.