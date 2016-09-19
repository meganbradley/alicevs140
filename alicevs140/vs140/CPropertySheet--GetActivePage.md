---
title: "CPropertySheet::GetActivePage"
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
ms.assetid: 179ad165-dff9-4eb9-955e-f841e836bd46
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::GetActivePage
Retrieves the property sheet window's active page.  
  
## Syntax  
  
```  
  
CPropertyPage* GetActivePage( ) const;  
  
```  
  
## Return Value  
 The pointer to the active page.  
  
## Remarks  
 Use this member function to perform some action on the active page.  
  
## Example  
 [!CODE [NVC_MFCDocView#135](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#135)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::GetPage](../vs140/CPropertySheet--GetPage.md)