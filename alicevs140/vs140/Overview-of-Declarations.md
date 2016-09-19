---
title: "Overview of Declarations"
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
ms.assetid: fcd2364c-c2a5-4fbf-9027-19dac4144cb5
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overview of Declarations
A "declaration" specifies the interpretation and attributes of a set of identifiers. A declaration that also causes storage to be reserved for the object or function named by the identifier is called a "definition." C declarations for variables, functions, and types have this syntax:  
  
## Syntax  
 `declaration`:  
 *declaration-specifiers* *attribute-seq*opt*init-declarator-list*opt**;**  
  
 /\* *attribute-seq*opt is Microsoft specific */  
  
 *declaration-specifiers*:  
 *storage-class-specifier declaration-specifiers*opt  
  
 *type-specifier declaration-specifiers*opt  
  
 *type-qualifier declaration-specifiers*opt  
  
 *init-declarator-list*:  
 *init-declarator*  
  
 *init-declarator-list* , *init-declarator*  
  
 *init-declarator*:  
 *declarator*  
  
 *declarator*  **=**  *initializer*  
  
> [!NOTE]
>  This syntax for `declaration` is not repeated in the following sections. Syntax in the following sections usually begins with the `declarator` nonterminal.  
  
 The declarations in the *init-declarator-list* contain the identifiers being named; *init* is an abbreviation for initializer. The *init-declarator-list* is a comma-separated sequence of declarators, each of which can have additional type information, or an initializer, or both. The `declarator` contains the identifiers, if any, being declared. The *declaration-specifiers* nonterminal consists of a sequence of type and storage-class specifiers that indicate the linkage, storage duration, and at least part of the type of the entities that the declarators denote. Therefore, declarations are made up of some combination of storage-class specifiers, type specifiers, type qualifiers, declarators, and initializers.  
  
 Declarations can contain one or more of the optional attributes listed in *attribute-seq*; *seq* is an abbreviation for sequence. These Microsoft-specific attributes perform a variety of functions, which are discussed in detail throughout this book.  
  
 In the general form of a variable declaration, *type-specifier* gives the data type of the variable. The *type-specifier* can be a compound, as when the type is modified by **const** or `volatile`. The `declarator` gives the name of the variable, possibly modified to declare an array or a pointer type. For example,  
  
```  
int const *fp;  
```  
  
 declares a variable named `fp` as a pointer to a nonmodifiable (**const**) `int` value. You can define more than one variable in a declaration by using multiple declarators, separated by commas.  
  
 A declaration must have at least one declarator, or its type specifier must declare a structure tag, union tag, or members of an enumeration. Declarators provide any remaining information about an identifier. A declarator is an identifier that can be modified with brackets (**[ ]**), asterisks (**\***), or parentheses ( **( )** ) to declare an array, pointer, or function type, respectively. When you declare simple variables (such as character, integer, and floating-point items), or structures and unions of simple variables, the `declarator` is just an identifier. For more information on declarators, see [Declarators and Variable Declarations](../vs140/Declarators-and-Variable-Declarations.md).  
  
 All definitions are implicitly declarations, but not all declarations are definitions. For example, variable declarations that begin with the `extern` storage-class specifier are "referencing," rather than "defining" declarations. If an external variable is to be referred to before it is defined, or if it is defined in another source file from the one where it is used, an `extern` declaration is necessary. Storage is not allocated by "referencing" declarations, nor can variables be initialized in declarations.  
  
 A storage class or a type (or both) is required in variable declarations. Except for `__declspec`, only one storage-class specifier is allowed in a declaration and not all storage-class specifiers are permitted in every context. The `__declspec` storage class is allowed with other storage-class specifiers, and it is allowed more than once. The storage-class specifier of a declaration affects how the declared item is stored and initialized, and which parts of a program can reference the item.  
  
 The *storage-class-specifier* terminals defined in C include **auto**, `extern`, **register**, **static**, and `typedef`. In addition, Microsoft C includes the *storage-class-specifier* terminal `__declspec`. All *storage-class-specifier* terminals except `typedef` and `__declspec` are discussed in [Storage Classes](../vs140/C-Storage-Classes.md). See [Typedef Declarations](../vs140/Typedef-Declarations.md) for information about `typedef`. See [Extended Storage-Class Attributes](../vs140/C-Extended-Storage-Class-Attributes.md) for information about `__declspec`.  
  
 The location of the declaration within the source program and the presence or absence of other declarations of the variable are important factors in determining the lifetime of variables. There can be multiple redeclarations but only one definition. However, a definition can appear in more than one translation unit. For objects with internal linkage, this rule applies separately to each translation unit, because internally linked objects are unique to a translation unit. For objects with external linkage, this rule applies to the entire program. See [Lifetime, Scope, Visibility, and Linkage](../vs140/Lifetime--Scope--Visibility--and-Linkage.md) for more information about visibility.  
  
 Type specifiers provide some information about the data types of identifiers. The default type specifier is `int`. For more information, see [Type Specifiers](../vs140/C-Type-Specifiers.md). Type specifiers can also define type tags, structure and union component names, and enumeration constants. For more information see [Enumeration Declarations](../vs140/C-Enumeration-Declarations.md), [Structure Declarations](../vs140/Structure-Declarations.md), and [Union Declarations](../vs140/Union-Declarations.md).  
  
 There are two *type-qualifier* terminals: **const** and `volatile`. These qualifiers specify additional properties of types that are relevant only when accessing objects of that type through l-values. For more information on **const** and `volatile`, see [Type Qualifiers](../vs140/Type-Qualifiers.md). For a definition of l-values, see [L-Value and R-Value Expressions](../vs140/L-Value-and-R-Value-Expressions.md).  
  
## See Also  
 [C Language Syntax Summary](../vs140/C-Language-Syntax-Summary.md)   
 [Declarations and Types](../vs140/Declarations-and-Types.md)   
 [Summary of Declarations](../vs140/Summary-of-Declarations.md)