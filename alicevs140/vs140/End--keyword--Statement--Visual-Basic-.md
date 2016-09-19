---
title: "End &lt;keyword&gt; Statement (Visual Basic)"
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
ms.assetid: 42d6e088-ab0f-4cda-88e8-fdce3e5fcf4f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# End &lt;keyword&gt; Statement (Visual Basic)
When followed by an additional keyword, terminates the definition of the statement block introduced by that keyword.  
  
## Syntax  
  
```  
End AddHandler  
End Class   
End Enum   
End Event   
End Function   
End Get   
End If   
End Interface   
End Module   
End Namespace   
End Operator   
End Property   
End RaiseEvent  
End RemoveHandler  
End Select   
End Set   
End Structure   
End Sub   
End SyncLock   
End Try   
End While   
End With  
```  
  
## Parts  
 `End`  
 Required. Terminates the definition of the programming element.  
  
 `AddHandler`  
 Required to terminate an `AddHandler` accessor begun by a matching `AddHandler` statement in a custom [Event Statement](../vs140/Event-Statement.md).  
  
 `Class`  
 Required to terminate a class definition begun by a matching [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md).  
  
 `Enum`  
 Required to terminate an enumeration definition begun by a matching [Enum Statement](../Topic/Enum%20Statement%20\(Visual%20Basic\).md).  
  
 `Event`  
 Required to terminate a `Custom` event definition begun by a matching [Event Statement](../vs140/Event-Statement.md).  
  
 `Function`  
 Required to terminate a `Function` procedure definition begun by a matching [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md). If execution encounters an `End``Function` statement, control returns to the calling code.  
  
 `Get`  
 Required to terminate a `Property` procedure definition begun by a matching [Get Statement](../vs140/Get-Statement.md). If execution encounters an `End``Get` statement, control returns to the statement requesting the property's value.  
  
 `If`  
 Required to terminate an `If`...`Then`...`Else` block definition begun by a matching `If` statement. See [If...Then...Else Statement](../Topic/If...Then...Else%20Statement%20\(Visual%20Basic\).md).  
  
 `Interface`  
 Required to terminate an interface definition begun by a matching [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md).  
  
 `Module`  
 Required to terminate a module definition begun by a matching [Module Statement](../Topic/Module%20Statement.md).  
  
 `Namespace`  
 Required to terminate a namespace definition begun by a matching [Namespace Statement](../Topic/Namespace%20Statement.md).  
  
 `Operator`  
 Required to terminate an operator definition begun by a matching [Operator Statement](../vs140/Operator-Statement.md).  
  
 `Property`  
 Required to terminate a property definition begun by a matching [Property Statement](../vs140/Property-Statement.md).  
  
 `RaiseEvent`  
 Required to terminate a `RaiseEvent` accessor begun by a matching `RaiseEvent` statement in a custom [Event Statement](../vs140/Event-Statement.md).  
  
 `RemoveHandler`  
 Required to terminate a `RemoveHandler` accessor begun by a matching `RemoveHandler` statement in a custom [Event Statement](../vs140/Event-Statement.md).  
  
 `Select`  
 Required to terminate a `Select`...`Case` block definition begun by a matching `Select` statement. See [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md).  
  
 `Set`  
 Required to terminate a `Property` procedure definition begun by a matching [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md). If execution encounters an `End``Set` statement, control returns to the statement setting the property's value.  
  
 `Structure`  
 Required to terminate a structure definition begun by a matching [Structure Statement](../Topic/Structure%20Statement.md).  
  
 `Sub`  
 Required to terminate a `Sub` procedure definition begun by a matching [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md). If execution encounters an `End``Sub` statement, control returns to the calling code.  
  
 `SyncLock`  
 Required to terminate a `SyncLock` block definition begun by a matching `SyncLock` statement. See [SyncLock Statement](../Topic/SyncLock%20Statement.md).  
  
 `Try`  
 Required to terminate a `Try`...`Catch`...`Finally` block definition begun by a matching `Try` statement. See [Try...Catch...Finally Statement](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md).  
  
 `While`  
 Required to terminate a `While` loop definition begun by a matching `While` statement. See [While...End While Statement](../Topic/While...End%20While%20Statement%20\(Visual%20Basic\).md).  
  
 `With`  
 Required to terminate a `With` block definition begun by a matching `With` statement. See [With...End With Statement](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md).  
  
## Remarks  
 The [End Statement](../vs140/End-Statement.md), without an additional keyword, terminates execution immediately.  
  
 When preceded by a number sign (`#`), the `End` keyword terminates a preprocessing block introduced by the corresponding directive.  
  
 `#End`  
 Required. Terminates the definition of the preprocessing block.  
  
 `#ExternalSource`  
 Required to terminate an external source block begun by a matching [#ExternalSource Directive](../vs140/#ExternalSource-Directive.md).  
  
 `#If`  
 Required to terminate a conditional compilation block begun by a matching `#If` directive. See [#If...Then...#Else Directives](../vs140/#If...Then...#Else-Directives.md).  
  
 `#Region`  
 Required to terminate a source region block begun by a matching [#Region Directive](../vs140/#Region-Directive.md).  
  
## Smart Device Developer Notes  
 The `End` statement, without an additional keyword, is not supported.  
  
## See Also  
 [End Statement](../vs140/End-Statement.md)