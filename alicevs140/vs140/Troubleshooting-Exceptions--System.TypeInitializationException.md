---
title: "Troubleshooting Exceptions: System.TypeInitializationException"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c77e81fd-1518-49a1-8213-3f169658f5f5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.TypeInitializationException
The exception that is thrown as a wrapper around the exception thrown by the class initializer.  
  
## Remarks  
 When a class initializer fails to initialize a type, a <xref:System.TypeInitializationException?qualifyHint=False> is created and passed a reference to the exception thrown by the type's class initializer. The <xref:System.Exception.InnerException?qualifyHint=False> property of the <xref:System.TypeInitializationException?qualifyHint=False> holds the underlying exception.  
  
## See Also  
 <xref:System.TypeInitializationException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)