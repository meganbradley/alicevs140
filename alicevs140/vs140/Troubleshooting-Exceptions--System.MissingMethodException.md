---
title: "Troubleshooting Exceptions: System.MissingMethodException"
ms.custom: na
ms.date: 09/19/2016
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
ms.assetid: 1ca4c351-ca26-4a6d-a5a1-c484ac193e2e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.MissingMethodException
A <xref:System.MissingMethodException?qualifyHint=False> exception is thrown when there is an attempt to dynamically access a method that does not exist.  
  
## Associated Tips  
 **If a method in a class library has been removed or renamed, recompile any assemblies that reference that method.**  
 This exception is typically thrown when an attempt is made to dynamically access a deleted or renamed method of an assembly that is not referenced by its strong name.  
  
## Remarks  
 If you are calling an unmanaged function, this exception is thrown if the CLR cannot find the module or function.  
  
## See Also  
 <xref:System.MissingMethodException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)   
 [Troubleshooting Interoperability](../vs140/Troubleshooting-Interoperability--Visual-Basic-.md)