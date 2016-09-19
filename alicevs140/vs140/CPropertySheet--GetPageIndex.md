---
title: "CPropertySheet::GetPageIndex"
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
ms.assetid: 1a7f7c96-7faf-4f91-9dbc-d880aa93d5e3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::GetPageIndex
Retrieves the index number of the specified page in the property sheet.  
  
## Syntax  
  
```  
  
      int GetPageIndex(  
   CPropertyPage* pPage   
);  
```  
  
#### Parameters  
 `pPage`  
 Points to the page with the index to be found. Cannot be **NULL**.  
  
## Return Value  
 The index number of a page.  
  
## Remarks  
 For example, you would use `GetPageIndex` to get the page index in order to use [SetActivePage](../vs140/CPropertySheet--SetActivePage.md) or [GetPage](../vs140/CPropertySheet--GetPage.md).  
  
## Example  
 See the example for [CPropertySheet::GetActivePage](../vs140/CPropertySheet--GetActivePage.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::SetActivePage](../vs140/CPropertySheet--SetActivePage.md)   
 [CPropertySheet::GetPage](../vs140/CPropertySheet--GetPage.md)