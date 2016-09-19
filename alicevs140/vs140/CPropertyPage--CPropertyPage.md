---
title: "CPropertyPage::CPropertyPage"
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
ms.assetid: 6c7ff2b8-e412-4eda-8015-e4fb76f3da7f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::CPropertyPage
Constructs a `CPropertyPage` object.  
  
## Syntax  
  
```  
  
      CPropertyPage( );   
explicit CPropertyPage(  
   UINT nIDTemplate,  
   UINT nIDCaption = 0,  
   DWORD dwSize = sizeof(PROPSHEETPAGE)  
);  
explicit CPropertyPage(  
   LPCTSTR lpszTemplateName,  
   UINT nIDCaption = 0,  
   DWORD dwSize = sizeof(PROPSHEETPAGE)  
);  
CPropertyPage(  
   UINT nIDTemplate,  
   UINT nIDCaption,  
   UINT nIDHeaderTitle,  
   UINT nIDHeaderSubTitle = 0,  
   DWORD dwSize = sizeof(PROPSHEETPAGE)  
);  
CPropertyPage(  
   LPCTSTR lpszTemplateName,  
   UINT nIDCaption,  
   UINT nIDHeaderTitle,  
   UINT nIDHeaderSubTitle = 0,  
   DWORD dwSize = sizeof(PROPSHEETPAGE)  
);  
```  
  
#### Parameters  
 `nIDTemplate`  
 ID of the template used for this page.  
  
 `nIDCaption`  
 ID of the name to be placed in the tab for this page. If 0, the name will be taken from the dialog template for this page.  
  
 `dwSize`  
 `lpszTemplateName`  
 Points to a string containing the name of the template for this page. Cannot be **NULL**.  
  
 `nIDHeaderTitle`  
 ID of the name to be placed in the title location of the property page header.  
  
 `nIDHeaderSubTitle`  
 ID of the name to be placed in the subtitle location of the property page header.  
  
## Remarks  
 The object is displayed after all of the following conditions are met:  
  
-   The page has been added to a property sheet using [CPropertySheet::AddPage](../vs140/CPropertySheet--AddPage.md).  
  
-   The property sheet's [DoModal](../vs140/CPropertySheet--DoModal.md) or [Create](../vs140/CPropertySheet--Create.md) function has been called.  
  
-   The user has selected (tabbed to) this page.  
  
 If you have multiple parameters (for example, if you are using an array), use [CPropertySheet::Construct](../vs140/CPropertySheet--Construct.md) instead of `CPropertyPage`.  
  
## Example  
 [!CODE [NVC_MFCDocView#113](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#113)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::Create](../vs140/CPropertySheet--Create.md)   
 [CPropertySheet::DoModal](../vs140/CPropertySheet--DoModal.md)   
 [CPropertySheet::AddPage](../vs140/CPropertySheet--AddPage.md)   
 [CPropertyPage::Construct](../vs140/CPropertyPage--Construct.md)