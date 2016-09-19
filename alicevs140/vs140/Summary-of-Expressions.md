---
title: "Summary of Expressions"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed448953-687a-4b57-a1cb-12967bd770ea
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Summary of Expressions
*primary-expression*:  
 *identifier*  
  
 *constant*  
  
 *string-literal*  
  
 **(**  *expression*  **)**  
  
 *expression*:  
 *assignment-expression*  
  
 *expression*  **,**  *assignment-expression*  
  
 *constant-expression*:  
 *conditional-expression*  
  
 *conditional-expression*:  
 *logical-OR-expression*  
  
 *logical-OR-expression*  **?**  *expression*  **:**  *conditional-expression*  
  
 *assignment-expression*:  
 *conditional-expression*  
  
 *unary-expression assignment-operator assignment-expression*  
  
 *postfix-expression*:  
 *primary-expression*  
  
 *postfix-expression*  **[**  *expression*  **]**  
  
 *postfix-expression*  **(**  *argument-expression-list* opt**)**  
  
 *postfix-expression*  **.**  *identifier*  
  
 *postfix-expression*  **–>**  *identifier*  
  
 *postfix-expression*  **++**  
  
 *postfix-expression*  **––**  
  
 *argument-expression-list*:  
 *assignment-expression*  
  
 *argument-expression-list*  **,**  *assignment-expression*  
  
 *unary-expression*:  
 *postfix-expression*  
  
 **++**  *unary-expression*  
  
 **––**  *unary-expression*  
  
 *unary-operator*  
  
 *cast-expression*  
  
 **sizeof**  *unary-expression*  
  
 **sizeof (**  *type-name*  **)**  
  
 *unary-operator*: one of  
 **& \* + – ~ !**  
  
 *cast-expression*:  
 *unary-expression*  
  
 **(**  *type-name*  **)**  *cast-expression*  
  
 *multiplicative-expression*:  
 *cast-expression*  
  
 *multiplicative-expression*  **\***  *cast-expression*  
  
 *multiplicative-expression*  **/**  *cast-expression*  
  
 *multiplicative-expression*  **%**  *cast-expression*  
  
 *additive-expression*:  
 *multiplicative-expression*  
  
 *additive-expression*  **+**  *multiplicative-expression*  
  
 *additive-expression*  **–**  *multiplicative-expression*  
  
 *shift-expression*:  
 *additive-expression*  
  
 *shift-expression*  **<<**  *additive-expression*  
  
 *shift-expression*  **>>**  *additive-expression*  
  
 *relational-expression*:  
 *shift-expression*  
  
 *relational-expression*  **<**  *shift-expression*  
  
 *relational-expression*  **>**  *shift-expression relational-expression*  **<=**  *shift-expression*  
  
 *relational-expression*  **>=**  *shift-expression*  
  
 *equality-expression*:  
 *relational-expression*  
  
 *equality-expression*  **==**  *relational-expression*  
  
 *equality-expression*  **!=**  *relational-expression*  
  
 *AND-expression*:  
 *equality-expression*  
  
 *AND-expression*  **&**  *equality-expression*  
  
 *exclusive-OR-expression*:  
 *AND-expression*  
  
 *exclusive-OR-expression*  **^**  *AND-expression*  
  
 *inclusive-OR-expression*:  
 *exclusive-OR-expression*  
  
 *inclusive-OR-expression*  **&#124;**  *exclusive-OR-expression*  
  
 *logical-AND-expression*:  
 *inclusive-OR-expression*  
  
 *logical-AND-expression*  **&&**  *inclusive-OR-expression*  
  
 *logical-OR-expression*:  
 *logical-AND-expression*  
  
 *logical-OR-expression*  **&#124;&#124;**  *logical-AND-expression*  
  
## See Also  
 [Phrase Structure Grammar](../vs140/Phrase-Structure-Grammar.md)