---
title: "Troubleshooting Exceptions: System.Net.CookieException"
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
ms.assetid: 7db6b962-cc5e-4b63-be65-894a8f186b38
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Exceptions: System.Net.CookieException
A <xref:System.Net.CookieException?qualifyHint=False> exception is thrown when an error is made adding a cookie to a cookie container.  
  
## Associated Tips  
 **Make sure the cookie size does not exceed the maximum allowed by the cookie container.**  
 This exception is thrown when an attempt is made to add a <xref:System.Net.Cookie?qualifyHint=False> with length greater than <xref:System.Net.CookieContainer.MaxCookieSize?qualifyHint=False> to a <xref:System.Net.CookieContainer?qualifyHint=False>. The default maximum cookie size is 4096 bytes.  
  
 **When setting the Name property for a cookie, make sure the value is not a null reference or empty string.**  
 The <xref:System.Net.Cookie.Name?qualifyHint=False> property must be initialized before using an instance of the <xref:System.Net.Cookie?qualifyHint=False> class. The following characters are reserved and cannot be used for this attribute value: equal sign, semicolon, comma, new line (\n), carriage return (\r), tab (\t). The dollar sign ($) character cannot be the first character.  
  
 **When setting the Port property for a cookie, make sure the value is valid and enclosed in double quotes.**  
 The <xref:System.Net.Cookie.Port?qualifyHint=False> attribute restricts the ports to which a cookie may be sent. The default value means no restriction. Setting the property to an empty string ("") restricts the port to the one used in the HTTP response. Otherwise the value must be a string in quotation marks that contains port values delineated with commas.  
  
 **When setting the Value property for a cookie, make sure the value is not null.**  
 The following characters are reserved and cannot be used for this property: semicolon, comma.  
  
## See Also  
 <xref:System.Net.CookieException?qualifyHint=False>   
 [How to: Find Out More About an Exception with the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)   
 [How to: Write a Cookie](assetId:///0b155ea3-ea96-401c-977e-81cbdf7bb486)