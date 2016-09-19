---
title: "My.Request Object"
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
ms.assetid: 93d5f0e2-6b60-4a2c-8652-d90216f6ad10
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# My.Request Object
Gets the <xref:System.Web.HttpRequest?qualifyHint=False> object for the requested page.  
  
## Remarks  
 The `My.Request` object contains information about the current HTTP request.  
  
 The `My.Request` object is available only for ASP.NET applications.  
  
## Example  
 The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.  
  
 [!CODE [VbVbalrMyWeb#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyWeb#1)]  
  
## See Also  
 <xref:System.Web.HttpRequest?qualifyHint=False>   
 [My.Response Object](../Topic/My.Response%20Object.md)