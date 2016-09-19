---
title: "Troubleshooting Exceptions: System.ArgumentNullException"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - JScript
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f21413c-d997-47c6-9b06-3d85a719d51b
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.ArgumentNullException
An <xref:System.ArgumentNullException?qualifyHint=False> exception is thrown when a null reference (`Nothing` in Visual Basic) is passed to a method that does not accept it as a valid argument.  
  
## Associated Tips  
 **Check arguments to make sure they are not null (Nothing in Visual Basic).**  
 A null reference is a reference to an object that does not exist, often because no instance of the object has been programmatically created.  
  
## Remarks  
 <xref:System.ArgumentNullException?qualifyHint=False> behaves identically to <xref:System.ArgumentException?qualifyHint=False>. It is provided so application code can differentiate between exceptions caused by null arguments and exceptions caused by arguments that are not null. For errors caused by arguments that are not null, see [Troubleshooting Exceptions: System.ArgumentOutOfRangeException](../Topic/Troubleshooting%20Exceptions:%20System.ArgumentOutOfRangeException.md).  
  
## See Also  
 <xref:System.ArgumentNullException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)