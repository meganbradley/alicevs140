---
title: "The project file &#39;&lt;filename&gt;&#39; cannot be updated"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ecd1e161-c51c-4aaa-ab80-8fc443bdad81
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# The project file &#39;&lt;filename&gt;&#39; cannot be updated
You are attempting to open a project created in an earlier version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. The project must be updated to the current format, but it cannot be updated because either the specified project file (.vbproj) is marked as read-only or the file is under source control and is currently locked by another user.  
  
### To correct this error  
  
1.  In File Explorer, locate the specified project file.  
  
2.  On the **File** menu, choose **Properties**.  
  
3.  In the **Properties** dialog box, uncheck the **Read-only** attribute.  
  
 If the file is under source code control and is locked by another user, wait until the file is available and check it out locally.  
  
## See Also  
 [NIB: Project Properties (Visual Studio)](assetId:///eb4c97ed-f667-4850-98d0-6e2a4d21bbca)