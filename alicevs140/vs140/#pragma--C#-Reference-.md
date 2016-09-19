---
title: "#pragma (C# Reference)"
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
ms.assetid: 5b7944cd-d402-46a1-ad8f-feffb2d83673
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #pragma (C# Reference)
`#pragma` gives the compiler special instructions for the compilation of the file in which it appears. The instructions must be supported by the compiler. In other words, you cannot use `#pragma` to create custom preprocessing instructions. The Microsoft C# compiler supports the following two `#pragma` instructions:  
  
 [#pragma warning](../vs140/#pragma-warning--C#-Reference-.md)  
  
 [#pragma checksum](../vs140/#pragma-checksum--C#-Reference-.md)  
  
## Syntax  
  
```  
#pragma pragma-name pragma-arguments  
```  
  
#### Parameters  
 `pragma-name`  
 The name of a recognized pragma.  
  
 `pragma-arguments`  
 Pragma-specific arguments.  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)   
 [#pragma warning](../vs140/#pragma-warning--C#-Reference-.md)   
 [#pragma checksum](../vs140/#pragma-checksum--C#-Reference-.md)