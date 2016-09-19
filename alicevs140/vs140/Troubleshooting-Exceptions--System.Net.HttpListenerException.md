---
title: "Troubleshooting Exceptions: System.Net.HttpListenerException"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1595c5b6-4710-4076-9bfc-9f70f52e679a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Net.HttpListenerException
An <xref:System.Net.HttpListenerException?qualifyHint=False> is thrown when an error occurs processing a Hypertext Transfer Protocol request.  
  
## Associated Tips  
 Make sure you are not attempting to register a URI prefix that is already registered.  
 If the URI prefix is already registered, this exception will occur.  
  
 Make sure your HTTP request is valid.  
 This exception is thrown by the <xref:System.Net.HttpListener?qualifyHint=False> class and its associated classes when an error occurs during the initialization of the <xref:System.Net.HttpListener?qualifyHint=False> or while creating or sending a response to an HTTP request.  
  
 If you are using the `HttpListenerPrefixCollection.Add` method, make sure the `uriPrefix` has not been already added.  
 This exception will be thrown if another <xref:System.Net.HttpListener?qualifyHint=False> has already added the prefix `uriPrefix`.  
  
## See Also  
 <xref:System.Net.HttpListenerException?qualifyHint=False>   
 <xref:System.Net.HttpListener?qualifyHint=False>   
 <xref:System.Net.HttpListenerPrefixCollection?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)