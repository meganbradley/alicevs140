---
title: "Error: The Web Server Could Not Find the Requested Resource"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ceeaf30-918c-42bb-ace1-96944530fef3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: The Web Server Could Not Find the Requested Resource
Due to security considerations, IIS has returned a generic error.  
  
 One possible cause is the security configuration of the server. IIS 6.0 and earlier versions used an add-on program, known as URLScan, to filter out suspicious and malformed requests. IIS 7.0 has built-in Request Filtering for the same purpose. In both cases, overly restrictive request filtering can prevent Visual Studio from debugging the server.  
  
 There are numerous possible causes of this error. A few of the most common causes include a problem with the IIS installation or configuration, the web site configuration, or permissions in the file system. You can try accessing the resource with a browser. Depending on how IIS is configured you might have to use a local browser on the server or inspect the IIS error log to get a detailed error message.  
  
 For more information on troubleshooting IIS, see [IIS Management and Administration](http://go.microsoft.com/fwlink/?LinkId=255872).  
  
## See Also  
 [UrlScan Security Tool](http://www.microsoft.com/technet/security/tools/urlscan.mspx)   
 [Error: The Web Server Has Been Locked Down and Is Blocking the DEBUG Verb](../vs140/Error--The-Web-Server-Has-Been-Locked-Down-and-Is-Blocking-the-DEBUG-Verb.md)