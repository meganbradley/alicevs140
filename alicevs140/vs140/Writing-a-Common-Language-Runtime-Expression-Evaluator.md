---
title: "Writing a Common Language Runtime Expression Evaluator"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd79d57f-8e0a-4e14-a417-0b1de28fa1b2
caps.latest.revision: 25
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Writing a Common Language Runtime Expression Evaluator
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 The expression evaluator (EE) is the part of a debug engine (DE) that handles the syntax and semantics of the programming language that produced the code being debugged. Expressions must be evaluated within the context of a programming language. For example, in some languages, the expression "A+B" means "the sum of A and B." In other languages, the same expression might mean "A or B." Thus, a separate EE must be written for each programming language that generates object code to be debugged in the Visual Studio IDE.  
  
 Some aspects of the Visual Studio debug package must interpret the code in the context of the programming language. For example, when execution halts at a breakpoint, any expressions that the user has typed into a **Watch** window must be evaluated and displayed. Also, the user can change the value of a local variable by typing an expression into a **Watch** window or into the **Immediate** window.  
  
## In This Section  
 [Common Language Runtime and Expression Evaluation](../vs140/Common-Language-Runtime-and-Expression-Evaluation.md)  
 Explains that when you are integrating proprietary programming language into the Visual Studio IDE, writing an EE capable of evaluating expressions within the context of the proprietary language allows you to compile to a Microsoft intermediate language (MSIL) without writing a debug engine.  
  
 [Expression Evaluator Architecture](../vs140/Expression-Evaluator-Architecture.md)  
 Discusses how to implement the required EE interfaces and call the common language runtime symbol provider (SP) and binder interfaces.  
  
 [Registering an Expression Evaluator](../Topic/Registering%20an%20Expression%20Evaluator.md)  
 Notes that the EE must register itself as a class factory with both the common language runtime and Visual Studio runtime environments.  
  
 [Implementing an Expression Evaluator](../vs140/Implementing-an-Expression-Evaluator.md)  
 Describes how the process of evaluating an expression includes the debug engine (DE), the symbol provider (SP), the binder object, and the expression evaluator (EE).  
  
 [Displaying Locals](../vs140/Displaying-Locals.md)  
 Describes how, when execution pauses, the debug package calls the DE to get a list of local variables and arguments.  
  
 [Evaluating a Watch Window Expression](../vs140/Evaluating-a-Watch-Window-Expression.md)  
 Documents how the Visual Studio debug package calls the DE to determine the current value of each expression in its watch list.  
  
 [Changing the Value of a Local](../vs140/Changing-the-Value-of-a-Local.md)  
 Explains that in changing the value of a local, each line of the Locals window has an associated object that provides the name, type, and current value of a local.  
  
 [Implementing Type Visualizers and Custom Viewers](../vs140/Implementing-Type-Visualizers-and-Custom-Viewers.md)  
 Explains which interface needs to be implemented by which component to support type visualizers and custom viewers.  
  
## See Also  
 [Visual Studio Debugging SDK](../vs140/Visual-Studio-Debugger-Extensibility.md)