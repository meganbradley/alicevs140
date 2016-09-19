---
title: "Breakpoints (Visual Studio SDK)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: acfcabed-9f2f-436c-ad18-7ca2f45d631b
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Breakpoints (Visual Studio SDK)
There are three types of breakpoints: pending, bound, and error.  
  
 **A pending breakpoint:**  
  
-   Is an abstraction that contains all the information needed to bind a breakpoint to one or more code contexts in one or more programs. Each time a program being debugged cause code to load, the debug engine checks all pending breakpoints to see if they can be bound.  
  
     A pending breakpoint itself never binds to code, but rather collects and is said to contain all the bound breakpoints that it generates.  
  
-   Is represented by an [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md) interface.  
  
 **A bound breakpoint:**  
  
-   Is an abstraction for a breakpoint associated with or bound to a single code context. Each bound breakpoint is generated in response to a pending breakpoint. A pending breakpoint can, however, generate more than one bound breakpoint.  
  
     When code is unloaded, a bound breakpoint can be unbound and discarded.  
  
-   Is represented by an [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md) interface.  
  
 **An error breakpoint:**  
  
-   Is an abstraction for describing an error in attempting to bind a pending breakpoint to a code context. An error breakpoint describes either an error in location or in the breakpoint expression itself. For more information, see [Binding Breakpoints](../vs140/Binding-Breakpoints.md).  
  
     The breakpoint error can be either an error or a warning.  
  
-   Is represented by an [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md) interface.  
  
## See Also  
 [Programs](../vs140/Programs.md)   
 [Debugger Concepts](../vs140/Debugger-Concepts.md)   
 [Code Context](../vs140/Code-Context.md)   
 [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)   
 [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md)