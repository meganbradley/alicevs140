---
title: "CPropertySheet::SetActivePage"
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
ms.assetid: 80505ec8-8c77-42f2-a226-322f83116a86
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::SetActivePage
Changes the active page.  
  
## Syntax  
  
```  
  
      BOOL SetActivePage(  
   int nPage   
);  
BOOL SetActivePage(  
   CPropertyPage* pPage   
);  
```  
  
#### Parameters  
 `nPage`  
 Index of the page to set. It must be between 0 and one less than the number of pages in the property sheet, inclusive.  
  
 `pPage`  
 Points to the page to set in the property sheet. It cannot be **NULL**.  
  
## Return Value  
 Nonzero if the property sheet is activated successfully; otherwise 0.  
  
## Remarks  
 For example, use `SetActivePage` if a user's action on one page should cause another page to become the active page.  
  
## Example  
 See the example for [CPropertySheet::GetActivePage](../vs140/CPropertySheet--GetActivePage.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)