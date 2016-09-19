---
title: "&#39;&lt;membername&gt;&#39; is not declared"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6704bed-bb76-47c6-ac28-09608d5e6912
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;membername&gt;&#39; is not declared
'`<membername>`' is not declared. `Debug` object functionality is available in `System.Diagnostics.Debug` in the `System` assembly.  
  
 The specified member name could not be found.  
  
 **Error ID:** BC30816  
  
### To correct this error  
  
1.  Verify the spelling of the member.  
  
2.  Use an `Imports` statement or fully qualify members defined in other namespaces. For example, the `WriteLine` function is declared in the `System.Diagnostics.Debug` namespace.  
  
## See Also  
 [Debugging in Visual Studio](../vs140/Debugging-in-Visual-Studio.md)