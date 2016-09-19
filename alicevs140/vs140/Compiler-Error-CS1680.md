---
title: "Compiler Error CS1680"
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
ms.assetid: 973da155-e6fa-4de8-94fd-7838f839a81f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1680
Invalid reference alias option: 'alias=' -- missing filename.  
  
 This error occurs when you use the `alias` feature with the **/reference** compiler option without specifying a valid file name.  
  
 The following sample generates CS1680.  
  
```  
// CS1680.cs  
// compile with: /reference:alias=  
// CS1680 expected  
// To resolve, specify the name of a file with an assembly manifest  
class MyClass {}  
  
```