---
title: "CPropertySheet::RemovePage"
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
ms.assetid: 2a48edeb-107f-40ad-9279-0629eed89749
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::RemovePage
Removes a page from the property sheet and destroys the associated window.  
  
## Syntax  
  
```  
void RemovePage(  
   CPropertyPage *pPage   
);  
void RemovePage(  
   int nPage   
);  
```  
  
#### Parameters  
 `pPage`  
 Points to the page to be removed from the property sheet. Cannot be `NULL`.  
  
 `nPage`  
 Index of the page to be removed. Must be between 0 and one less than the number of pages in the property sheet, inclusive.  
  
## Remarks  
 The [CPropertyPage](../vs140/CPropertyPage-Class.md) object itself is not destroyed until the owner of the `CPropertySheet` window is closed.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::AddPage](../vs140/CPropertySheet--AddPage.md)