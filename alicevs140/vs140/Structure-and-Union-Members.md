---
title: "Structure and Union Members"
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
ms.assetid: bb1fe304-af49-4f98-808d-afdc99b3e319
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Structure and Union Members
A "member-selection expression" refers to members of structures and unions. Such an expression has the value and type of the selected member.  
  
```  
  
postfix-expression  
.  
identifier  
postfix-expression  
–>  
identifier  
  
```  
  
 This list describes the two forms of the member-selection expressions:  
  
1.  In the first form, *postfix-expression* represents a value of `struct` or **union** type, and *identifier* names a member of the specified structure or union. The value of the operation is that of *identifier* and is an l-value if *postfix-expression* is an l-value. See [L-Value and R-Value Expressions](../vs140/L-Value-and-R-Value-Expressions.md) for more information.  
  
2.  In the second form, *postfix-expression* represents a pointer to a structure or union, and *identifier* names a member of the specified structure or union. The value is that of *identifier* and is an l-value.  
  
 The two forms of member-selection expressions have similar effects.  
  
 In fact, an expression involving the member-selection operator (**–>**) is a shorthand version of an expression using the period (**.**) if the expression before the period consists of the indirection operator (**\***) applied to a pointer value. Therefore,  
  
```  
  
expression  
–>  
identifier  
  
```  
  
 is equivalent to  
  
```  
  
(*  
expression  
) .  
identifier  
  
```  
  
 when *expression* is a pointer value.  
  
## Examples  
 The following examples refer to this structure declaration. For information about the indirection operator (**\***) used in these examples, see [Indirection and Address-of Operators](../vs140/Indirection-and-Address-of-Operators.md).  
  
```  
struct pair   
{  
    int a;  
    int b;  
    struct pair *sp;  
} item, list[10];  
```  
  
 A member-selection expression for the `item` structure looks like this:  
  
```  
item.sp = &item;  
```  
  
 In the example above, the address of the `item` structure is assigned to the `sp` member of the structure. This means that `item` contains a pointer to itself.  
  
```  
(item.sp)–>a = 24;  
```  
  
 In this example, the pointer expression `item.sp` is used with the member-selection operator (**–>**) to assign a value to the member `a`.  
  
```  
list[8].b = 12;  
```  
  
 This statement shows how to select an individual structure member from an array of structures.  
  
## See Also  
 [Member Access Operators: . and ->](../vs140/Member-Access-Operators--.-and---.md)