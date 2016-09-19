---
title: "The -moduleassemblyname option may only be specified when building a target of type &#39;module&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: The /moduleassemblyname option may only be specified when building a target of type &#39;module&#39;
ms.assetid: 2ebc577b-3464-40cc-8788-9fc9d3b4f928
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# The -moduleassemblyname option may only be specified when building a target of type &#39;module&#39;
The Visual Basic compiler has been passed the `/moduleassemblyname` compiler option when the `/target` option is set to a value other than `module`.  
  
 **Error ID:** BC2030  
  
### To correct this error  
  
1.  Remove the `/moduleassemblyname` compiler option or set the `/target` option to `module`.  
  
## See Also  
 [/target (Visual Basic)](../Topic/-target%20\(Visual%20Basic\).md)   
 [/moduleassemblyname](../vs140/-moduleassemblyname.md)   
 [Visual Basic Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)