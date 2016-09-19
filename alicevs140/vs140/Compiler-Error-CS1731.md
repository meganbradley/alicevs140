---
title: "Compiler Error CS1731"
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
ms.assetid: 267b32aa-a692-4a54-8654-0540ee36c0a0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1731
Cannot convert 'expression' to delegate because some of the return types in the block are not implicitly convertible to the delegate return type.  
  
 This error is generated when a lambda expression or anonymous method has a return type that is not compatible with the delegate's return type.  
  
### To correct this error  
  
1.  Change the return type of either the delegate or the expression.  
  
## Example  
 The following code generates CS1731:  
  
```  
class CS1731  
{  
    delegate double D();  
    D d = () => { return "Who knows the real sword of Gryffindor?"; };  
}  
```