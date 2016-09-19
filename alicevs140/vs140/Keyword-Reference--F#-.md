---
title: "Keyword Reference (F#)"
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
ms.assetid: fa987a3b-7247-4aa5-bb96-2606b77e3d23
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Keyword Reference (F#)
This topic contains links to information about all F# language keywords.  
  
## F# Keyword Table  
 The following table shows all F# keywords in alphabetical order, together with brief descriptions and links to relevant topics that contain more information.  
  
|Keyword|Link|Description|  
|-------------|----------|-----------------|  
|`abstract`|[Members (F#)](../vs140/Members--F#-.md)<br /><br /> [Abstract Classes](../vs140/Abstract-Classes--F#-.md)|Indicates a method that either has no implementation in the type in which it is declared or that is virtual and has a default implementation.|  
|`and`|[Let Bindings](../vs140/let-Bindings--F#-.md)<br /><br /> [Members (F#)](../vs140/Members--F#-.md)<br /><br /> [Constraints](../vs140/Constraints--F#-.md)|Used in mutually recursive bindings, in property declarations, and with multiple constraints on generic parameters.|  
|`as`|[Classes (F#)](../vs140/Classes--F#-.md)<br /><br /> [Patterns](../vs140/Pattern-Matching--F#-.md)|Used to give the current class object an object name. Also used to give a name to a whole pattern within a pattern match.|  
|`assert`|[Assertions (F#)](../Topic/Assertions%20\(F%23\).md)|Used to verify code during debugging.|  
|`base`|[Classes (F#)](../vs140/Classes--F#-.md)<br /><br /> [Inheritance (F#)](../Topic/Inheritance%20\(F%23\).md)|Used as the name of the base class object.|  
|`begin`|[Verbose Syntax (F#)](../vs140/Verbose-Syntax--F#-.md)|In verbose syntax, indicates the start of a code block.|  
|`class`|[Classes (F#)](../vs140/Classes--F#-.md)|In verbose syntax, indicates the start of a class definition.|  
|`default`|[Members (F#)](../vs140/Members--F#-.md)|Indicates an implementation of an abstract method; used together with an abstract method declaration to create a virtual method.|  
|`delegate`|[Delegates (F#)](../vs140/Delegates--F#-.md)|Used to declare a delegate.|  
|`do`|[Do Bindings](../vs140/do-Bindings--F#-.md)<br /><br /> [Loops: the for...to Expression](../vs140/Loops--for...to-Expression--F#-.md)<br /><br /> [Loops: the for...in Expression](../vs140/Loops--for...in-Expression--F#-.md)<br /><br /> [Loops: while...do](../vs140/Loops--while...do-Expression--F#-.md)|Used in looping constructs or to execute imperative code.|  
|`done`|[Verbose Syntax (F#)](../vs140/Verbose-Syntax--F#-.md)|In verbose syntax, indicates the end of a block of code in a looping expression.|  
|`downcast`|[Casting and Conversions (F#)](../vs140/Casting-and-Conversions--F#-.md)|Used to convert to a type that is lower in the inheritance chain.|  
|`downto`|[Loops: the for...to Expression](../vs140/Loops--for...to-Expression--F#-.md)|In a `for` expression, used when counting in reverse.|  
|`elif`|[Conditional Expressions: if...then...else](../vs140/Conditional-Expressions--if...-then...else--F#-.md)|Used in conditional branching. A short form of `else if`.|  
|`else`|[Conditional Expressions: if...then...else](../vs140/Conditional-Expressions--if...-then...else--F#-.md)|Used in conditional branching.|  
|`end`|[Structures](../vs140/Structures--F#-.md)<br /><br /> [Discriminated Unions](../vs140/Discriminated-Unions--F#-.md)<br /><br /> [Records](../vs140/Records--F#-.md)<br /><br /> [Type Extensions](../vs140/Type-Extensions--F#-.md)<br /><br /> [Verbose Syntax (F#)](../vs140/Verbose-Syntax--F#-.md)|In type definitions and type extensions, indicates the end of a section of member definitions.<br /><br /> In verbose syntax, used to specify the end of a code block that starts with the `begin` keyword.|  
|`exception`|[Exception Handling (F#)](../vs140/Exception-Handling--F#-.md)<br /><br /> [Exception Types (F#)](../Topic/Exception%20Types%20\(F%23\).md)|Used to declare an exception type.|  
|`extern`|[External Functions](../vs140/External-Functions--F#-.md)|Indicates that a declared program element is defined in another binary or assembly.|  
|`false`|[Primitive Types (F#)](../Topic/Primitive%20Types%20\(F%23\).md)|Used as a Boolean literal.|  
|`finally`|[Exceptions: the try...finally Expression](../vs140/Exceptions--The-try...finally-Expression--F#-.md)|Used together with `try` to introduce a block of code that executes regardless of whether an exception occurs.|  
|`for`|[Loops: the for...to Expression](../vs140/Loops--for...to-Expression--F#-.md)<br /><br /> [Loops: the for...in Expression](../vs140/Loops--for...in-Expression--F#-.md)|Used in looping constructs.|  
|`fun`|[Lambda Expressions](../vs140/Lambda-Expressions--The-fun-Keyword--F#-.md)|Used in lambda expressions, also known as anonymous functions.|  
|`function`|[Match Expressions](../vs140/Match-Expressions--F#-.md)<br /><br /> [Lambda Expressions](../vs140/Lambda-Expressions--The-fun-Keyword--F#-.md)|Used as a shorter alternative to the `fun` keyword and a `match` expression in a lambda expression that has pattern matching on a single argument.|  
|`global`|[Namespaces (F#)](../vs140/Namespaces--F#-.md)|Used to reference the top-level .NET namespace.|  
|`if`|[Conditional Expressions: if...then...else](../vs140/Conditional-Expressions--if...-then...else--F#-.md)|Used in conditional branching constructs.|  
|`in`|[Loops: the for...in Expression](../vs140/Loops--for...in-Expression--F#-.md)<br /><br /> [Verbose Syntax (F#)](../vs140/Verbose-Syntax--F#-.md)|Used for sequence expressions and, in verbose syntax, to separate expressions from bindings.|  
|`inherit`|[Inheritance (F#)](../Topic/Inheritance%20\(F%23\).md)|Used to specify a base class or base interface.|  
|`inline`|[Functions (F#)](../vs140/Functions--F#-.md)<br /><br /> [Inline Functions](../vs140/Inline-Functions--F#-.md)|Used to indicate a function that should be integrated directly into the caller's code.|  
|`interface`|[Interfaces (F#)](../vs140/Interfaces--F#-.md)|Used to declare and implement interfaces.|  
|`internal`|[Access Control (F#)](../vs140/Access-Control--F#-.md)|Used to specify that a member is visible inside an assembly but not outside it.|  
|`lazy`|[Lazy Computations](../vs140/Lazy-Computations--F#-.md)|Used to specify a computation that is to be performed only when a result is needed.|  
|`let`|[Let Bindings](../vs140/let-Bindings--F#-.md)|Used to associate, or bind, a name to a value or function.|  
|`let!`|[Asynchronous Workflows](../Topic/Asynchronous%20Workflows%20\(F%23\).md)<br /><br /> [Computation Expressions](../Topic/Computation%20Expressions%20\(F%23\).md)|Used in asynchronous workflows to bind a name to the result of an asynchronous computation, or, in other computation expressions, used to bind a name to a result, which is of the computation type.|  
|`match`|[Pattern Matching](../vs140/Match-Expressions--F#-.md)|Used to branch by comparing a value to a pattern.|  
|`member`|[Members (F#)](../vs140/Members--F#-.md)|Used to declare a property or method in an object type.|  
|`module`|[Modules (F#)](../vs140/Modules--F#-.md)|Used to associate a name with a group of related types, values, and functions, to logically separate it from other code.|  
|`mutable`|[Let Bindings](../vs140/let-Bindings--F#-.md)|Used to declare a variable, that is, a value that can be changed.|  
|`namespace`|[Namespaces (F#)](../vs140/Namespaces--F#-.md)|Used to associate a name with a group of related types and modules, to logically separate it from other code.|  
|`new`|[Object Creation and Initialization](../vs140/Constructors--F#-.md)<br /><br /> [Constraints](../vs140/Constraints--F#-.md)|Used to declare, define, or invoke a constructor that creates or that can create an object.<br /><br /> Also used in generic parameter constraints to indicate that a type must have a certain constructor.|  
|`not`|[Symbol and Operator Reference](../vs140/Symbol-and-Operator-Reference--F#-.md)<br /><br /> [Constraints](../vs140/Constraints--F#-.md)|Not actually a keyword. However, `not struct` in combination is used as a generic parameter constraint.|  
|`null`|[Null Values](../vs140/Null-Values--F#-.md)<br /><br /> [Constraints](../vs140/Constraints--F#-.md)|Indicates the absence of an object.<br /><br /> Also used in generic parameter constraints.|  
|`of`|[Discriminated Unions (F#)](../vs140/Discriminated-Unions--F#-.md)<br /><br /> [Delegates (F#)](../vs140/Delegates--F#-.md)<br /><br /> [Exception Types (F#)](../Topic/Exception%20Types%20\(F%23\).md)|Used in discriminated unions to indicate the type of categories of values, and in delegate and exception declarations.|  
|`open`|[Referencing Code: the open Keyword](../vs140/Import-Declarations--The-open-Keyword--F#-.md)|Used to make the contents of a namespace or module available without qualification.|  
|`or`|[Symbol and Operator Reference](../vs140/Symbol-and-Operator-Reference--F#-.md)<br /><br /> [Constraints (F#)](../vs140/Constraints--F#-.md)|Used with Boolean conditions as a Boolean `or` operator. Equivalent to `&#124;&#124;`.<br /><br /> Also used in member constraints.|  
|`override`|[Members (F#)](../vs140/Members--F#-.md)|Used to implement a version of an abstract or virtual method that differs from the base version.|  
|`private`|[Access Control (F#)](../vs140/Access-Control--F#-.md)|Restricts access to a member to code in the same type or module.|  
|`public`|[Access Control (F#)](../vs140/Access-Control--F#-.md)|Allows access to a member from outside the type.|  
|`rec`|[Functions (F#)](../vs140/Functions--F#-.md)|Used to indicate that a function is recursive.|  
|`return`|[Asynchronous Workflows](../Topic/Asynchronous%20Workflows%20\(F%23\).md)<br /><br /> [Computation Expressions](../Topic/Computation%20Expressions%20\(F%23\).md)|Used to indicate a value to provide as the result of a computation expression.|  
|`return!`|[Computation Expressions](../Topic/Computation%20Expressions%20\(F%23\).md)<br /><br /> [Asynchronous Workflows](../Topic/Asynchronous%20Workflows%20\(F%23\).md)|Used to indicate a computation expression that, when evaluated, provides the result of the containing computation expression.|  
|`select`|[Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md)|Used in query expressions to specify what fields or columns to extract. Note that this is a contextual keyword, which means that it is not actually a reserved word and it only acts like a keyword in appropriate context.|  
|`static`|[Members (F#)](../vs140/Members--F#-.md)|Used to indicate a method or property that can be called without an instance of a type, or a value member that is shared among all instances of a type.|  
|`struct`|[Structures (F#)](../vs140/Structures--F#-.md)<br /><br /> [Constraints (F#)](../vs140/Constraints--F#-.md)|Used to declare a structure type.<br /><br /> Also used in generic parameter constraints.<br /><br /> Used for OCaml compatibility in module definitions.|  
|`then`|[Conditional Expressions: if...then...else](../vs140/Conditional-Expressions--if...-then...else--F#-.md)<br /><br /> [Object Creation and Initialization](../vs140/Constructors--F#-.md)|Used in conditional expressions.<br /><br /> Also used to perform side effects after object construction.|  
|`to`|[Loops: the for...to Expression](../vs140/Loops--for...to-Expression--F#-.md)|Used in `for` loops to indicate a range.|  
|`true`|[Primitive Types (F#)](../Topic/Primitive%20Types%20\(F%23\).md)|Used as a Boolean literal.|  
|`try`|[Exceptions: try...with Expression](../vs140/Exceptions--The-try...with-Expression--F#-.md)<br /><br /> [Exceptions: the try...finally Expression](../vs140/Exceptions--The-try...finally-Expression--F#-.md)|Used to introduce a block of code that might generate an exception. Used together with `with` or `finally`.|  
|`type`|[F# Types](../vs140/F#-Types.md)<br /><br /> [Classes (F#)](../vs140/Classes--F#-.md)<br /><br /> [Records](../vs140/Records--F#-.md)<br /><br /> [Structures (F#)](../vs140/Structures--F#-.md)<br /><br /> [Enumerations](../vs140/Enumerations--F#-.md)<br /><br /> [Discriminated Unions](../vs140/Discriminated-Unions--F#-.md)<br /><br /> [Type Abbreviations](../vs140/Type-Abbreviations--F#-.md)<br /><br /> [Units of Measure](../vs140/Units-of-Measure--F#-.md)|Used to declare a class, record, structure, discriminated union, enumeration type, unit of measure, or type abbreviation.|  
|`upcast`|[Casting and Conversions (F#)](../vs140/Casting-and-Conversions--F#-.md)|Used to convert to a type that is higher in the inheritance chain.|  
|`use`|[Resource Management (F#)](../Topic/Resource%20Management:%20The%20use%20Keyword%20\(F%23\).md)|Used instead of `let` for values that require `Dispose` to be called to free resources.|  
|`use!`|[Computation Expressions](../Topic/Computation%20Expressions%20\(F%23\).md)<br /><br /> [Asynchronous Workflows](../Topic/Asynchronous%20Workflows%20\(F%23\).md)|Used instead of `let!` in asynchronous workflows and other computation expressions for values that require `Dispose` to be called to free resources.|  
|`val`|[Fields: the val keyword](../Topic/Explicit%20Fields:%20The%20val%20Keyword%20\(F%23\).md)<br /><br /> [Signatures (F#)](../vs140/Signatures--F#-.md)<br /><br /> [Members (F#)](../vs140/Members--F#-.md)|Used in a signature to indicate a value, or in a type to declare a member, in limited situations.|  
|`void`|[Primitive Types (F#)](../Topic/Primitive%20Types%20\(F%23\).md)|Indicates the .NET `void` type. Used when interoperating with other .NET languages.|  
|`when`|[Constraints (F#)](../vs140/Constraints--F#-.md)|Used for Boolean conditions (*when guards*) on pattern matches and to introduce a constraint clause for a generic type parameter.|  
|`while`|[Loops: while...do Expression](../vs140/Loops--while...do-Expression--F#-.md)|Introduces a looping construct.|  
|`with`|[Pattern Matching](../vs140/Match-Expressions--F#-.md)<br /><br /> [Object Expressions](../vs140/Object-Expressions--F#-.md)<br /><br /> [Type Extensions](../vs140/Type-Extensions--F#-.md)<br /><br /> [Exceptions: try...with Expression](../vs140/Exceptions--The-try...with-Expression--F#-.md)|Used together with the `match` keyword in pattern matching expressions. Also used in object expressions, record copying expressions, and type extensions to introduce member definitions, and to introduce exception handlers.|  
|`yield`|[Sequences (F#)](../Topic/Sequences%20\(F%23\).md)|Used in a sequence expression to produce a value for a sequence.|  
|`yield!`|[Computation Expressions](../Topic/Computation%20Expressions%20\(F%23\).md)<br /><br /> [Asynchronous Workflows](../Topic/Asynchronous%20Workflows%20\(F%23\).md)|Used in a computation expression to append the result of a given computation expression to a collection of results for the containing computation expression.|  
  
 In addition, the following tokens are reserved in F# because they are keywords in the OCaml language:  
  
|||||||||  
|-|-|-|-|-|-|-|-|  
|`asr`|`land`|`lor`|`lsl`|`lsr`|`lxor`|`mod`|`sig`|  
  
 If you use the `--mlcompatibility` compiler option, these keywords are available for use as identifiers.  
  
 The following tokens are reserved as keywords for future expansion of the F# language:  
  
||||||||  
|-|-|-|-|-|-|-|  
|`atomic`|`break`|`checked`|`component`|`const`|`constraint`|`constructor`|  
|`continue`|`eager`|`event`|`external`|`fixed`|`functor`|`include`|  
|`method`|`mixin`|`object`|`parallel`|`process`|`protected`|`pure`|  
|`sealed`|`tailcall`|`trait`|`virtual`|`volatile`|||  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [Symbol and Operator Reference](../vs140/Symbol-and-Operator-Reference--F#-.md)   
 [Compiler Options](../vs140/Compiler-Options--F#-.md)