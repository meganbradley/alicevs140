---
title: "Match Expressions (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: dab9b934-5528-4283-8986-794d832f0a0b
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Match Expressions (F#)
The `match` expression provides branching control that is based on the comparison of an expression with a set of patterns.  
  
## Syntax  
  
```  
// Match expression.  
match test-expression with  
    | pattern1 [ when condition ] -> result-expression1  
    | pattern2 [ when condition ] -> result-expression2  
    | ...  
  
// Pattern matching function.  
function  
    | pattern1 [ when condition ] -> result-expression1  
    | pattern2 [ when condition ] -> result-expression2  
    | ...  
```  
  
## Remarks  
 The pattern matching expressions allow for complex branching based on the comparison of a test expression with a set of patterns. In the `match` expression, the `test-expression` is compared with each pattern in turn, and when a match is found, the corresponding `result-expression` is evaluated and the resulting value is returned as the value of the match expression.  
  
 The pattern matching function shown in the previous syntax is a lambda expression in which pattern matching is performed immediately on the argument. The pattern matching function shown in the previous syntax is equivalent to the following.  
  
 fun `arg` ->  
  
 match `arg` with  
  
 &#124; `pattern1` [ when `condition` ] -> `result-expression1`  
  
 &#124; `pattern2` [ when `condition` ]-> `result-expression2`  
  
 &#124; ...  
  
 For more information about lambda expressions, see [Lambda Expressions: The fun keyword](../vs140/Lambda-Expressions--The-fun-Keyword--F#-.md).  
  
 The whole set of patterns should cover all the possible matches of the input variable. Frequently, you use the wildcard pattern (_) as the last pattern to match any previously unmatched input values.  
  
 The following code illustrates some of the ways in which the `match` expression is used. For a reference and examples of all the possible patterns that can be used, see [Patterns](../vs140/Pattern-Matching--F#-.md).  
  
 [!CODE [FsLangRef2#4601](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4601)]  
  
## Guards on Patterns  
 You can use a `when` clause to specify an additional condition that the variable must satisfy to match a pattern. Such a clause is referred to as a *guard*. The expression following the `when` keyword is not evaluated unless a match is made to the pattern associated with that guard.  
  
 The following example illustrates the use of a guard to specify a numeric range for a variable pattern. Note that multiple conditions are combined by using Boolean operators.  
  
 [!CODE [FsLangRef2#4602](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4602)]  
  
 Note that because values other than literals cannot be used in the pattern, you must use a `when` clause if you have to compare some part of the input against a value. This is shown in the following code.  
  
 [!CODE [FsLangRef2#4603](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4603)]  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [Active Patterns](../vs140/Active-Patterns--F#-.md)