---
title: "CMFCPropertySheet::AddPage"
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
ms.assetid: 72759478-a414-4abc-bd5b-7bf07e3c52e7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertySheet::AddPage
Adds a page to the property sheet.  
  
## Syntax  
  
```  
void AddPage(  
   CPropertyPage* pPage   
);  
```  
  
#### Parameters  
 [in] `pPage`  
 Pointer to a page object. This parameter cannot be `NULL`.  
  
## Remarks  
 This method adds the specified property page as the rightmost tab in the property sheet. Therefore, use this method to add pages in left-to-right order.  
  
 If the property sheet is in the style of Microsoft Outlook, the framework displays a list of navigation buttons at the left of the property sheet. After this method adds a property page, it adds a corresponding button to the list. To display a property page, click its corresponding button. For more information about styles of property sheets, see [CMFCPropertySheet::SetLook](../vs140/CMFCPropertySheet--SetLook.md).  
  
## Requirements  
 **Header:** afxpropertysheet.h  
  
## See Also  
 [CMFCPropertySheet Class](../vs140/CMFCPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::AddPage](../vs140/CPropertySheet--AddPage.md)   
 [CMFCPropertySheet::SetLook](../vs140/CMFCPropertySheet--SetLook.md)