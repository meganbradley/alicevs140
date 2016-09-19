---
title: "Accessing Application Web Services (Visual Basic)"
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
ms.assetid: 8ad5405b-e771-42b1-82d3-ce97af2cea9e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Accessing Application Web Services (Visual Basic)
The `My.WebServices` object provides an instance of each Web service referenced by the current project. Each instance is instantiated on demand. You can access these Web services through the properties of the `My.WebServices` object. The name of the property is the same as the name of the Web service that the property accesses. Any class that inherits from <xref:System.Web.Services.Protocols.SoapHttpClientProtocol?qualifyHint=False> is a Web service.  
  
## Tasks  
 The following table lists possible ways to access Web services referenced by an application.  
  
|||  
|-|-|  
|To|See|  
|Call a Web service|[My.WebServices Object](../Topic/My.WebServices%20Object.md)|  
|Call a Web service asynchronously and handle an event when it completes|[How to: Call a Web Service Asynchronously](../vs140/How-to--Call-a-Web-Service-Asynchronously--Visual-Basic-.md)|  
  
## See Also  
 [My.WebServices Object](../Topic/My.WebServices%20Object.md)