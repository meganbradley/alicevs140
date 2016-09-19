---
title: "Compiler Error CS2034"
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
ms.assetid: 72f2b785-ee23-4a1b-b12d-42d19c324d5e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2034
A /reference option that declares an extern alias can only have one filename. To specify multiple aliases or filenames, use multiple /reference options.  
  
 To specify two aliases and/or file names, use two **/reference** options, like this:  
  
## Example  
 The following code will generate error CS2034.  
  
```  
// CS2034.cs  
// compile with: /r:A1=cs2034a1.dll;A2=cs2034a2.dll  
// to fix, compile with: /r:A1=cs2034a1.dll /r:A2=cs2034a2.dll  
// CS2034  
extern alias A1;  
extern alias A2;  
using System;  
```