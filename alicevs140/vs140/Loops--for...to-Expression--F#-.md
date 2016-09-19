---
title: "Loops: for...to Expression (F#)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: bbefda86-6785-40bc-ac02-fe4faf96aac2
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Loops: for...to Expression (F#)
The `for...to` expression is used to iterate in a loop over a range of values of a loop variable.  
  
## Syntax  
  
```  
for identifier = start [ to | downto ] finish do  
   body-expression  
```  
  
## Remarks  
 The type of the identifier is inferred from the type of the *start* and *finish* expressions. Types for these expressions must be 32-bit integers.  
  
 Although technically an expression, `for...to` is more like a traditional statement in an imperative programming language. The return type for the *body-expression* must be `unit`. The following examples show various uses of the `for...to` expression.  
  
 [!CODE [FsLangRef2#5101](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#5101)]  
  
 The output of the previous code is as follows.  
  
```  
1 2 3 4 5 6 7 8 9 10  
10 9 8 7 6 5 4 3 2 1  
2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18  
```  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [Loops: for .. in Expression](../vs140/Loops--for...in-Expression--F#-.md)   
 [Loops: while...do Expression](../vs140/Loops--while...do-Expression--F#-.md)