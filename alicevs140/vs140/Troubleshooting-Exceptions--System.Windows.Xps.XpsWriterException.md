---
title: "Troubleshooting Exceptions: System.Windows.Xps.XpsWriterException"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b9fbb94-ed67-44f2-82bb-af5cb5ada1ef
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Windows.Xps.XpsWriterException
An <xref:System.Windows.Xps.XpsWriterException?qualifyHint=False> exception is thrown when a method of either an <xref:System.Windows.Xps.XpsDocumentWriter?qualifyHint=False> or a <xref:System.Windows.Xps.VisualsToXpsDocument?qualifyHint=False> object is called that is incompatible with the current state of the object.  
  
## Remarks  
 For example, this exception is thrown if the `CancelAsync` method of either object type is called when the object is not performing an asynchronous write operation.  
  
## See Also  
 <xref:System.Windows.Xps.XpsWriterException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)