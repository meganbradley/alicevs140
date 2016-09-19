---
title: "CPropertyPage::QuerySiblings"
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
ms.assetid: 5af187fd-f583-4fea-9d0e-ba52f64e899d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::QuerySiblings
Call this member function to forward a message to each page in the property sheet.  
  
## Syntax  
  
```  
  
      LRESULT QuerySiblings(  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `wParam`  
 Specifies additional message-dependent information.  
  
 `lParam`  
 Specifies additional message-dependent information  
  
## Return Value  
 The nonzero value from a page in the property sheet, or 0 if all pages return a value of 0.  
  
## Remarks  
 If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.  
  
## Example  
 [!CODE [NVC_MFCDocView#124](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#124)]  
  
 [!CODE [NVC_MFCDocView#125](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#125)]  
  
 [!CODE [NVC_MFCDocView#126](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#126)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)