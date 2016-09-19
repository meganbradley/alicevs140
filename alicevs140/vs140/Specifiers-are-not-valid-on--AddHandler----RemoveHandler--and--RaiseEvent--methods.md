---
title: "Specifiers are not valid on &#39;AddHandler&#39;, &#39;RemoveHandler&#39; and &#39;RaiseEvent&#39; methods"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2eaf5a6f-d201-4f9b-bcdf-12170cb44791
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifiers are not valid on &#39;AddHandler&#39;, &#39;RemoveHandler&#39; and &#39;RaiseEvent&#39; methods
The `AddHandler`, `RemoveHandler`, and `RaiseEvent` method declarations cannot be modified with keywords such as `Public` or `ReadOnly`. Only modifiable declarations can contain such keywords.  
  
 **Error ID:** BC31135  
  
### To correct this error  
  
-   Remove the keyword from the method declaration.  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [AddHandler - delete](assetId:///fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](assetId:///35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [RaiseEvent - delete](assetId:///7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [NIB Keywords (Visual Basic)](assetId:///3a6fda51-6ade-4862-a407-1c305c3906ec)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)