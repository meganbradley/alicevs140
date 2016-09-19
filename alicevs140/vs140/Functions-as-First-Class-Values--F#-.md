---
title: "Functions as First-Class Values (F#)"
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
ms.assetid: a9669418-52e3-4fa4-b04f-99d0d4b3f1fa
caps.latest.revision: 38
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Functions as First-Class Values (F#)
A defining characteristic of functional programming languages is the elevation of functions to first-class status. You should be able to do with a function whatever you can do with values of the other built-in types, and be able to do so with a comparable degree of effort.  
  
 Typical measures of first-class status include the following:  
  
-   Can you bind an identifier to the value? That is, can you give it a name?  
  
-   Can you store the value in a data structure, such as a list?  
  
-   Can you pass the value as an argument in a function call?  
  
-   Can you return the value as the value of a function call?  
  
 The last two measures define what are known as *higher-order operations* or *higher-order functions*. Higher-order functions accept functions as arguments and return functions as the value of function calls. These operations support such mainstays of functional programming as mapping functions and composition of functions.  
  
## Give the Value a Name  
 If a function is a first-class value, you must be able to name it, just as you can name integers, strings, and other built-in types. This is referred to in functional programming literature as binding an identifier to a value. F# uses [let expressions](../vs140/let-Bindings--F#-.md) to bind names to values: `let <identifier> = <value>`. The following code shows two examples.  
  
 [!CODE [FsConTour#20](../CodeSnippet/VS_Snippets_Fsharp/fscontour#20)]  
  
 You can name a function just as easily. The following example defines a function named `squareIt` by binding the identifier `squareIt` to the [lambda expression](../vs140/Lambda-Expressions--The-fun-Keyword--F#-.md)`fun n -> n * n`. Function `squareIt` has one parameter, `n`, and it returns the square of that parameter.  
  
 [!CODE [FsConTour#21](../CodeSnippet/VS_Snippets_Fsharp/fscontour#21)]  
  
 F# provides the following more concise syntax to achieve the same result with less typing.  
  
 [!CODE [FsConTour#22](../CodeSnippet/VS_Snippets_Fsharp/fscontour#22)]  
  
 The examples that follow mostly use the first style, `let <function-name> = <lambda-expression>`, to emphasize the similarities between the declaration of functions and the declaration of other types of values. However, all the named functions can also be written with the concise syntax. Some of the examples are written in both ways.  
  
## Store the Value in a Data Structure  
 A first-class value can be stored in a data structure. The following code shows examples that store values in lists and in tuples.  
  
 [!CODE [FsConTour#23](../CodeSnippet/VS_Snippets_Fsharp/fscontour#23)]  
  
 To verify that a function name stored in a tuple does in fact evaluate to a function, the following example uses the `fst` and `snd` operators to extract the first and second elements from tuple `funAndArgTuple`. The first element in the tuple is `squareIt` and the second element is `num`. Identifier `num` is bound in a previous example to integer 10, a valid argument for the `squareIt` function. The second expression applies the first element in the tuple to the second element in the tuple: `squareIt num`.  
  
 [!CODE [FsConTour#24](../CodeSnippet/VS_Snippets_Fsharp/fscontour#24)]  
  
 Similarly, just as identifier `num` and integer 10 can be used interchangeably, so can identifier `squareIt` and lambda expression `fun n -> n * n`.  
  
 [!CODE [FsConTour#25](../CodeSnippet/VS_Snippets_Fsharp/fscontour#25)]  
  
## Pass the Value as an Argument  
 If a value has first-class status in a language, you can pass it as an argument to a function. For example, it is common to pass integers and strings as arguments. The following code shows integers and strings passed as arguments in F#.  
  
 [!CODE [FsConTour#26](../CodeSnippet/VS_Snippets_Fsharp/fscontour#26)]  
  
 If functions have first-class status, you must be able to pass them as arguments in the same way. Remember that this is the first characteristic of higher-order functions.  
  
 In the following example, function `applyIt` has two parameters, `op` and `arg`. If you send in a function that has one parameter for `op` and an appropriate argument for the function to `arg`, the function returns the result of applying `op` to `arg`. In the following example, both the function argument and the integer argument are sent in the same way, by using their names.  
  
 [!CODE [FsConTour#27](../CodeSnippet/VS_Snippets_Fsharp/fscontour#27)]  
  
 The ability to send a function as an argument to another function underlies common abstractions in functional programming languages, such as map or filter operations. A map operation, for example, is a higher-order function that captures the computation shared by functions that step through a list, do something to each element, and then return a list of the results. You might want to increment each element in a list of integers, or to square each element, or to change each element in a list of strings to uppercase. The error-prone part of the computation is the recursive process that steps through the list and builds a list of the results to return. That part is captured in the mapping function. All you have to write for a particular application is the function that you want to apply to each list element individually (adding, squaring, changing case). That function is sent as an argument to the mapping function, just as `squareIt` is sent to `applyIt` in the previous example.  
  
 F# provides map methods for most collection types, including [lists](../vs140/Collections.List-Module--F#-.md), [arrays](../Topic/Collections.Array%20Module%20\(F%23\).md), and [sets](../vs140/Collections.Set-Module--F#-.md). The following examples use lists. The syntax is `List.map <the function> <the list>`.  
  
 [!CODE [FsConTour#28](../CodeSnippet/VS_Snippets_Fsharp/fscontour#28)]  
  
 For more information, see [Lists](../Topic/Lists%20\(F%23\).md).  
  
## Return the Value from a Function Call  
 Finally, if a function has first-class status in a language, you must be able to return it as the value of a function call, just as you return other types, such as integers and strings.  
  
 The following function calls return integers and display them.  
  
 [!CODE [FsConTour#29](../CodeSnippet/VS_Snippets_Fsharp/fscontour#29)]  
  
 The following function call returns a string.  
  
 [!CODE [FsConTour#30](../CodeSnippet/VS_Snippets_Fsharp/fscontour#30)]  
  
 The following function call, declared inline, returns a Boolean value. The value displayed is `True`.  
  
 [!CODE [FsConTour#31](../CodeSnippet/VS_Snippets_Fsharp/fscontour#31)]  
  
 The ability to return a function as the value of a function call is the second characteristic of higher-order functions. In the following example, `checkFor` is defined to be a function that takes one argument, `item`, and returns a new function as its value. The returned function takes a list as its argument, `lst`, and searches for `item` in `lst`. If `item` is present, the function returns `true`. If `item` is not present, the function returns `false`. As in the previous section, the following code uses a provided list function, [List.exists](../vs140/List.exists--T--Function--F#-.md), to search the list.  
  
 [!CODE [FsConTour#32](../CodeSnippet/VS_Snippets_Fsharp/fscontour#32)]  
  
 The following code uses `checkFor` to create a new function that takes one argument, a list, and searches for 7 in the list.  
  
 [!CODE [FsConTour#33](../CodeSnippet/VS_Snippets_Fsharp/fscontour#33)]  
  
 The following example uses the first-class status of functions in F# to declare a function, `compose`, that returns a composition of two function arguments.  
  
 [!CODE [FsConTour#34](../CodeSnippet/VS_Snippets_Fsharp/fscontour#34)]  
  
> [!NOTE]
>  For an even shorter version, see the following section, "Curried Functions."  
  
 The following code sends two functions as arguments to `compose`, both of which take a single argument of the same type. The return value is a new function that is a composition of the two function arguments.  
  
 [!CODE [FsConTour#35](../CodeSnippet/VS_Snippets_Fsharp/fscontour#35)]  
  
> [!NOTE]
>  F# provides two operators, `<<` and `>>`, that compose functions. For example, `let squareAndDouble2 = doubleIt << squareIt` is equivalent to `let squareAndDouble = compose doubleIt squareIt` in the previous example.  
  
 The following example of returning a function as the value of a function call creates a simple guessing game. To create a game, call `makeGame` with the value that you want someone to guess sent in for `target`. The return value from function `makeGame` is a function that takes one argument (the guess) and reports whether the guess is correct.  
  
 [!CODE [FsConTour#36](../CodeSnippet/VS_Snippets_Fsharp/fscontour#36)]  
  
 The following code calls `makeGame`, sending the value `7` for `target`. Identifier `playGame` is bound to the returned lambda expression. Therefore, `playGame` is a function that takes as its one argument a value for `guess`.  
  
 [!CODE [FsConTour#37](../CodeSnippet/VS_Snippets_Fsharp/fscontour#37)]  
  
## Curried Functions  
 Many of the examples in the previous section can be written more concisely by taking advantage of the implicit *currying* in F# function declarations. Currying is a process that transforms a function that has more than one parameter into a series of embedded functions, each of which has a single parameter. In F#, functions that have more than one parameter are inherently curried. For example, `compose` from the previous section can be written as shown in the following concise style, with three parameters.  
  
 [!CODE [FsConTour#38](../CodeSnippet/VS_Snippets_Fsharp/fscontour#38)]  
  
 However, the result is a function of one parameter that returns a function of one parameter that in turn returns another function of one parameter, as shown in `compose4curried`.  
  
 [!CODE [FsConTour#39](../CodeSnippet/VS_Snippets_Fsharp/fscontour#39)]  
  
 You can access this function in several ways. Each of the following examples returns and displays 18. You can replace `compose4` with `compose4curried` in any of the examples.  
  
 [!CODE [FsConTour#40](../CodeSnippet/VS_Snippets_Fsharp/fscontour#40)]  
  
 To verify that the function still works as it did before, try the original test cases again.  
  
 [!CODE [FsConTour#41](../CodeSnippet/VS_Snippets_Fsharp/fscontour#41)]  
  
> [!NOTE]
>  You can restrict currying by enclosing parameters in tuples. For more information, see "Parameter Patterns" in [Parameters and Arguments](../Topic/Parameters%20and%20Arguments%20\(F%23\).md).  
  
 The following example uses implicit currying to write a shorter version of `makeGame`. The details of how `makeGame` constructs and returns the `game` function are less explicit in this format, but you can verify by using the original test cases that the result is the same.  
  
 [!CODE [FsConTour#42](../CodeSnippet/VS_Snippets_Fsharp/fscontour#42)]  
  
 For more information about currying, see "Partial Application of Arguments" in [Functions](../vs140/Functions--F#-.md).  
  
## Identifier and Function Definition Are Interchangeable  
 The variable name `num` in the previous examples evaluates to the integer 10, and it is no surprise that where `num` is valid, 10 is also valid. The same is true of function identifiers and their values: anywhere the name of the function can be used, the lambda expression to which it is bound can be used.  
  
 The following example defines a `Boolean` function called `isNegative`, and then uses the name of the function and the definition of the function interchangeably. The next three examples all return and display `False`.  
  
 [!CODE [FsConTour#43](../CodeSnippet/VS_Snippets_Fsharp/fscontour#43)]  
  
 To take it one step further, substitute the value that `applyIt` is bound to for `applyIt`.  
  
 [!CODE [FsConTour#44](../CodeSnippet/VS_Snippets_Fsharp/fscontour#44)]  
  
## Functions Are First-Class Values in F#  
 The examples in the previous sections demonstrate that functions in F# satisfy the criteria for being first-class values in F#:  
  
-   You can bind an identifier to a function definition.  
  
     [!CODE [FsConTour#21](../CodeSnippet/VS_Snippets_Fsharp/fscontour#21)]  
  
-   You can store a function in a data structure.  
  
     [!CODE [FsConTour#45](../CodeSnippet/VS_Snippets_Fsharp/fscontour#45)]  
  
-   You can pass a function as an argument.  
  
     [!CODE [FsConTour#46](../CodeSnippet/VS_Snippets_Fsharp/fscontour#46)]  
  
-   You can return a function as the value of a function call.  
  
     [!CODE [FsConTour#32](../CodeSnippet/VS_Snippets_Fsharp/fscontour#32)]  
  
 For more information about F#, see [F# Language Reference](../Topic/F%23%20Language%20Reference.md).  
  
## Example  
  
### Description  
 The following code contains all the examples in this topic.  
  
### Code  
 [!CODE [FsConTour#47](../CodeSnippet/VS_Snippets_Fsharp/fscontour#47)]  
  
## See Also  
 [Lists](../Topic/Lists%20\(F%23\).md)   
 [Tuples](../Topic/Tuples%20\(F%23\).md)   
 [Functions](../vs140/Functions--F#-.md)   
 [let Bindings](../vs140/let-Bindings--F#-.md)   
 [lambda Expressions](../vs140/Lambda-Expressions--The-fun-Keyword--F#-.md)