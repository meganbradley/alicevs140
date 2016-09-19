---
title: "COleCmdUI::Enable"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: d04464d4-bbeb-480d-b414-b2f7a0d76495
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCmdUI::Enable
Call this function to set the command flag of the `COleCmdUI` object to **OLECOMDF_ENABLED**, which tells the interface the command is available and enabled, or to clear the command flag.  
  
## Syntax  
  
```  
  
      virtual void Enable(   
   BOOL bOn    
);  
```  
  
#### Parameters  
 `bOn`  
 Indicates whether the command associated with the `COleCmdUI` object should be enabled or disabled. Nonzero enables the command; 0 disables the command.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [COleCmdUI Class](../vs140/COleCmdUI-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)