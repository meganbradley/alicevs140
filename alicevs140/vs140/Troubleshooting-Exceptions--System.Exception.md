---
title: "Troubleshooting Exceptions: System.Exception"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc15931a-9323-47c6-a42f-55d0534b939a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Exception
Represents errors that occur during application execution. This is the base class for all exceptions.  
  
## Associated Tips  
 **Check the InnerException property for more information.**  
 To fix the error, you might need information about the inner (or previous) exception that led to the current exception. The current exception's <xref:System.Exception.InnerException?qualifyHint=False> property contains the inner exception. You can use the **View Detail** link in the **Exception Assistant** dialog box to access the <xref:System.Exception.InnerException?qualifyHint=False> property.  
  
 **Temporarily turn off Just My Code debugging.**  
 The exception may have occurred in code that you did not write. To debug that code, you may have to turn off Just My Code debugging. For more information, see [General, Debugging, Options Dialog Box](../vs140/General--Debugging--Options-Dialog-Box.md).  
  
## See Also  
 <xref:System.Exception?qualifyHint=False>   
 <xref:System.Exception.InnerException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)   
 [How to: Break When an Exception is Thrown](../vs140/How-to--Break-When-an-Exception-is-Thrown.md)   
 [General, Debugging, Options Dialog Box](../vs140/General--Debugging--Options-Dialog-Box.md)