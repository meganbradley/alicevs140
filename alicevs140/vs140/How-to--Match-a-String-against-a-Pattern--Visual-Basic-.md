---
title: "How to: Match a String against a Pattern (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 19a83804-b5af-4739-928b-ac93e64e457f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Match a String against a Pattern (Visual Basic)
If you want to find out if an expression of the [String Data Type (Visual Basic)](../Topic/String%20Data%20Type%20\(Visual%20Basic\).md) satisfies a pattern, then you can use the [Like Operator](../vs140/Like-Operator--Visual-Basic-.md).  
  
 `Like` takes two operands. The left operand is a string expression, and the right operand is a string containing the pattern to be used for matching. `Like` returns a `Boolean` value indicating whether the string expression satisfies the pattern.  
  
 You can match each character in the string expression against a specific character, a wildcard character, a character list, or a character range. The positions of the specifications in the pattern string correspond to the positions of the characters to be matched in the string expression.  
  
### To match a character in the string expression against a specific character  
  
-   Put the specific character directly in the pattern string. Certain special characters must be enclosed in brackets (`[ ]`). For more information, see [Like Operator](../vs140/Like-Operator--Visual-Basic-.md).  
  
     The following example tests whether `myString` consists exactly of the single character `H`.  
  
     [!CODE [VbVbalrOperators#70](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#70)]  
  
### To match a character in the string expression against a wildcard character  
  
-   Put a question mark (`?`) in the pattern string. Any valid character in this position makes a successful match.  
  
     The following example tests whether `myString` consists of the single character `W` followed by exactly two characters of any values.  
  
     [!CODE [VbVbalrOperators#71](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#71)]  
  
### To match a character in the string expression against a list of characters  
  
-   Put brackets (`[ ]`) in the pattern string, and inside the brackets put the list of characters. Do not separate the characters with commas or any other separator. Any single character in the list makes a successful match.  
  
     The following example tests whether `myString` consists of any valid character followed by exactly one of the characters `A`, `C`, or `E`.  
  
     [!CODE [VbVbalrOperators#72](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#72)]  
  
     Note that this match is case-sensitive.  
  
### To match a character in the string expression against a range of characters  
  
-   Put brackets (`[ ]`) in the pattern string, and inside the brackets put the lowest and highest characters in the range, separated by a hyphen (`–`). Any single character within the range makes a successful match.  
  
     The following example tests whether `myString` consists of the characters `num` followed by exactly one of the characters `i`, `j`, `k`, `l`, `m`, or `n`.  
  
     [!CODE [VbVbalrOperators#73](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#73)]  
  
     Note that this match is case-sensitive.  
  
## Matching Empty Strings  
 `Like` treats the sequence `[]` as a zero-length string (`""`). You can use `[]` to test whether the entire string expression is empty, but you cannot use it to test if a particular position in the string expression is empty. If an empty position is one of the options you need to test for, you can use `Like` more than once.  
  
#### To match a character in the string expression against a list of characters or no character  
  
1.  Call the `Like` operator twice on the same string expression, and connect the two calls with either the [Or Operator (Visual Basic)](../vs140/Or-Operator--Visual-Basic-.md) or the [OrElse Operator](../vs140/OrElse-Operator--Visual-Basic-.md).  
  
2.  In the pattern string for the first `Like` clause, include the character list, enclosed in brackets (`[ ]`).  
  
3.  In the pattern string for the second `Like` clause, do not put any character at the position in question.  
  
     The following example tests the seven-digit telephone number `phoneNum` for exactly three numeric digits, followed by a space, a hyphen (`–`), a period (`.`), or no character at all, followed by exactly four numeric digits.  
  
     [!CODE [VbVbalrOperators#74](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#74)]  
  
## See Also  
 [Comparison Operators](../Topic/Comparison%20Operators%20\(Visual%20Basic\).md)   
 [Operators and Expressions](../vs140/Operators-and-Expressions-in-Visual-Basic.md)   
 [Like Operator](../vs140/Like-Operator--Visual-Basic-.md)   
 [String Data Type (Visual Basic)](../Topic/String%20Data%20Type%20\(Visual%20Basic\).md)