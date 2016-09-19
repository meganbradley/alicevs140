---
title: "Compiler Error CS0268"
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
ms.assetid: a4faca71-8b4a-4f22-a89e-59d92ced48cb
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0268
Imported type 'type' is invalid. It contains a circular base class dependency.  
  
 This error occurs if a type imported from another language has a circular base class dependency. Such a type cannot be used in a C# program. To resolve this error, check types imported from other languages in any referenced assemblies or modules.