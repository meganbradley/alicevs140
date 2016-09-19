---
title: "CPropertySheet::AddPage"
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
ms.assetid: 98d45386-f4d0-4fa1-b589-682902f770e8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::AddPage
Adds the supplied page with the rightmost tab in the property sheet.  
  
## Syntax  
  
```  
  
      void AddPage(  
   CPropertyPage *pPage   
);  
```  
  
#### Parameters  
 `pPage`  
 Points to the page to be added to the property sheet. Cannot be **NULL**.  
  
## Remarks  
 Add pages to the property sheet in the left-to-right order you want them to appear.  
  
 `AddPage` adds the [CPropertyPage](../vs140/CPropertyPage--CPropertyPage.md) object to the `CPropertySheet` object's list of pages but does not actually create the window for the page. The framework postpones creation of the window for the page until the user selects that page.  
  
 When you add a property page using `AddPage`, the `CPropertySheet` is the parent of the `CPropertyPage`. To gain access to the property sheet from the property page, call [CWnd::GetParent](../vs140/CWnd--GetParent.md).  
  
 It is not necessary to wait until creation of the property sheet window to call `AddPage`. Typically, you will call `AddPage` before calling [DoModal](../vs140/CPropertySheet--DoModal.md) or [Create](../vs140/CPropertySheet--Create.md).  
  
 If you call `AddPage` after displaying the property page, the tab row will reflect the newly added page.  
  
## Example  
 [!CODE [NVC_MFCDocView#129](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#129)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::RemovePage](../vs140/CPropertySheet--RemovePage.md)