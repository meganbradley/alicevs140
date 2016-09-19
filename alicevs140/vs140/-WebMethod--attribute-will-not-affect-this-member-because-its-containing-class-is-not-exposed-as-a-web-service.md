---
title: "&#39;WebMethod&#39; attribute will not affect this member because its containing class is not exposed as a web service"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 20b09f6a-b61a-4d89-9ca5-4632b5e68e65
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;WebMethod&#39; attribute will not affect this member because its containing class is not exposed as a web service
The <xref:System.Web.Services.WebMethodAttribute?qualifyHint=False> attribute makes a method callable from remote Web clients, but only when the method's class derives from <xref:System.Web.Services.WebService?qualifyHint=False>.  
  
 **Error ID:** BC30771  
  
### To correct this error  
  
-   Change the class to derive from <xref:System.Web.Services.WebService?qualifyHint=False>.  
  
     — or —  
  
-   Remove the <xref:System.Web.Services.WebMethodAttribute?qualifyHint=False> attribute from the method.  
  
## See Also  
 [NIB: Walkthrough: Creating a Web Service Using Visual Basic or Visual C#](assetId:///295f4c3f-9540-4bd1-b1cc-3e9cb9675cc7)