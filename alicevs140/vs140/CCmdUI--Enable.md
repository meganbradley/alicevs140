---
title: "CCmdUI::Enable"
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
ms.assetid: b07c2867-fb1f-423b-bd1b-c0da88247b7e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdUI::Enable
Call this member function to enable or disable the user-interface item for this command.  
  
## Syntax  
  
```  
  
      virtual void Enable(  
   BOOL bOn = TRUE   
);  
```  
  
#### Parameters  
 `bOn`  
 **TRUE** to enable the item, **FALSE** to disable it.  
  
## Example  
 [!CODE [NVC_MFCDocView#46](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#46)]  
  
 [!CODE [NVC_MFCDocView#47](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#47)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdUI Class](../vs140/CCmdUI-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdUI::SetCheck](../vs140/CCmdUI--SetCheck.md)