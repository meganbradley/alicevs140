---
title: "CCmdUI::SetText"
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
ms.assetid: 1a396105-1aef-4fb3-a22c-24bea4605beb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdUI::SetText
Call this member function to set the text of the user-interface item for this command.  
  
## Syntax  
  
```  
  
      virtual void SetText(  
   LPCTSTR lpszText   
);  
```  
  
#### Parameters  
 `lpszText`  
 A pointer to a text string.  
  
## Example  
 [!CODE [NVC_MFCDocView#48](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#48)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdUI Class](../vs140/CCmdUI-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdUI::Enable](../vs140/CCmdUI--Enable.md)