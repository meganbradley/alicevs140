---
title: "Using Delegates (C# Programming Guide)"
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
ms.assetid: 99a2fc27-a32e-4a34-921c-e65497520eec
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Delegates (C# Programming Guide)
A [delegate](../vs140/delegate--C#-Reference-.md) is a type that safely encapsulates a method, similar to a function pointer in C and C++. Unlike C function pointers, delegates are object-oriented, type safe, and secure. The type of a delegate is defined by the name of the delegate. The following example declares a delegate named `Del` that can encapsulate a method that takes a [string](../Topic/string%20\(C%23%20Reference\).md) as an argument and returns [void](../vs140/void--C#-Reference-.md):  
  
 [!CODE [csProgGuideDelegates#21](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#21)]  
  
 A delegate object is normally constructed by providing the name of the method the delegate will wrap, or with an [anonymous Method](../vs140/Anonymous-Methods--C#-Programming-Guide-.md). Once a delegate is instantiated, a method call made to the delegate will be passed by the delegate to that method. The parameters passed to the delegate by the caller are passed to the method, and the return value, if any, from the method is returned to the caller by the delegate. This is known as invoking the delegate. An instantiated delegate can be invoked as if it were the wrapped method itself. For example:  
  
 [!CODE [csProgGuideDelegates#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#22)]  
  
 [!CODE [csProgGuideDelegates#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#23)]  
  
 Delegate types are derived from the <xref:System.Delegate?qualifyHint=False> class in the .NET Framework. Delegate types are [sealed](../vs140/sealed--C#-Reference-.md)—they cannot be derived from— and it is not possible to derive custom classes from <xref:System.Delegate?qualifyHint=False>. Because the instantiated delegate is an object, it can be passed as a parameter, or assigned to a property. This allows a method to accept a delegate as a parameter, and call the delegate at some later time. This is known as an asynchronous callback, and is a common method of notifying a caller when a long process has completed. When a delegate is used in this fashion, the code using the delegate does not need any knowledge of the implementation of the method being used. The functionality is similar to the encapsulation interfaces provide.  
  
 Another common use of callbacks is defining a custom comparison method and passing that delegate to a sort method. It allows the caller's code to become part of the sort algorithm. The following example method uses the `Del` type as a parameter:  
  
 [!CODE [csProgGuideDelegates#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#24)]  
  
 You can then pass the delegate created above to that method:  
  
 [!CODE [csProgGuideDelegates#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#25)]  
  
 and receive the following output to the console:  
  
 `The number is: 3`  
  
 Using the delegate as an abstraction, `MethodWithCallback` does not need to call the console directly—it does not have to be designed with a console in mind. What `MethodWithCallback` does is simply prepare a string and pass the string to another method. This is especially powerful since a delegated method can use any number of parameters.  
  
 When a delegate is constructed to wrap an instance method, the delegate references both the instance and the method. A delegate has no knowledge of the instance type aside from the method it wraps, so a delegate can refer to any type of object as long as there is a method on that object that matches the delegate signature. When a delegate is constructed to wrap a static method, it only references the method. Consider the following declarations:  
  
 [!CODE [csProgGuideDelegates#26](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#26)]  
  
 Along with the static `DelegateMethod` shown previously, we now have three methods that can be wrapped by a `Del` instance.  
  
 A delegate can call more than one method when invoked. This is referred to as multicasting. To add an extra method to the delegate's list of methods—the invocation list—simply requires adding two delegates using the addition or addition assignment operators ('+' or '+='). For example:  
  
 [!CODE [csProgGuideDelegates#27](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#27)]  
  
 At this point `allMethodsDelegate` contains three methods in its invocation list—`Method1`, `Method2`, and `DelegateMethod`. The original three delegates, `d1`, `d2`, and `d3`, remain unchanged. When `allMethodsDelegate` is invoked, all three methods are called in order. If the delegate uses reference parameters, the reference is passed sequentially to each of the three methods in turn, and any changes by one method are visible to the next method. When any of the methods throws an exception that is not caught within the method, that exception is passed to the caller of the delegate and no subsequent methods in the invocation list are called. If the delegate has a return value and/or out parameters, it returns the return value and parameters of the last method invoked. To remove a method from the invocation list, use the decrement or decrement assignment operator ('-' or '-='). For example:  
  
 [!CODE [csProgGuideDelegates#28](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#28)]  
  
 Because delegate types are derived from `System.Delegate`, the methods and properties defined by that class can be called on the delegate. For example, to find the number of methods in a delegate's invocation list, you may write:  
  
 [!CODE [csProgGuideDelegates#29](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#29)]  
  
 Delegates with more than one method in their invocation list derive from <xref:System.MulticastDelegate?qualifyHint=False>, which is a subclass of `System.Delegate`. The above code works in either case because both classes support `GetInvocationList`.  
  
 Multicast delegates are used extensively in event handling. Event source objects send event notifications to recipient objects that have registered to receive that event. To register for an event, the recipient creates a method designed to handle the event, then creates a delegate for that method and passes the delegate to the event source. The source calls the delegate when the event occurs. The delegate then calls the event handling method on the recipient, delivering the event data. The delegate type for a given event is defined by the event source. For more, see [Events (C#)](../Topic/Events%20\(C%23%20Programming%20Guide\).md).  
  
 Comparing delegates of two different types assigned at compile-time will result in a compilation error. If the delegate instances are statically of the type `System.Delegate`, then the comparison is allowed, but will return false at run time. For example:  
  
 [!CODE [csProgGuideDelegates#30](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#30)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Delegates (C# Programming Guide)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)   
 [Covariance and Contravariance in Delegates (C# Programming Guide)](../vs140/Using-Variance-in-Delegates--C#-and-Visual-Basic-.md)   
 [Variance in Generic Delegates](../vs140/Variance-in-Delegates--C#-and-Visual-Basic-.md)   
 [Using Covariance and Contravariance for Func and Action Generic Delegates](../vs140/Using-Variance-for-Func-and-Action-Generic-Delegates--C#-and-Visual-Basic-.md)   
 [Events (C#)](../Topic/Events%20\(C%23%20Programming%20Guide\).md)