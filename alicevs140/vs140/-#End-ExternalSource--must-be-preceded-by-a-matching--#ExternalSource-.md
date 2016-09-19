---
title: "&#39;#End ExternalSource&#39; must be preceded by a matching &#39;#ExternalSource&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f011673d-eced-46a7-a08e-d54d86c8a76b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;#End ExternalSource&#39; must be preceded by a matching &#39;#ExternalSource&#39;
The `#ExternalSource` directive references outside code, enabling the compiler to accurately report when exceptions occur within that code. An `#ExternalSource` block must begin with `#ExternalSource` and end with `#End ExternalSource`.  
  
 **Error ID:** BC30578  
  
### To correct this error  
  
1.  Add `#ExternalSource` to the appropriate location in your code.  
  
2.  Remove `#End ExternalSource` if it is unnecessary.  
  
## See Also  
 [#ExternalSource Directive](../vs140/#ExternalSource-Directive.md)   
 [NOTINBUILD Conditional Compilation (Visual Basic)](assetId:///ad1e35e0-935e-4a35-a2ae-738bcf2a9240)