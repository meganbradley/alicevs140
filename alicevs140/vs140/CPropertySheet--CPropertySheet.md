---
title: "CPropertySheet::CPropertySheet"
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
ms.assetid: 25c29c0e-ef35-4877-aaa5-e47cc68dbe6b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::CPropertySheet
Constructs a `CPropertySheet` object.  
  
## Syntax  
  
```  
  
      CPropertySheet( );   
explicit CPropertySheet(  
   UINT nIDCaption,  
   CWnd* pParentWnd = NULL,  
   UINT iSelectPage = 0   
);  
explicit CPropertySheet(  
   LPCTSTR pszCaption,  
   CWnd* pParentWnd = NULL,  
   UINT iSelectPage = 0   
);  
CPropertySheet(  
   UINT nIDCaption,  
   CWnd* pParentWnd,  
   UINT iSelectPage,  
   HBITMAP hbmWatermark,  
   HPALETTE hpalWatermark = NULL,  
   HBITMAP hbmHeader = NULL   
);  
CPropertySheet(  
   LPCTSTR pszCaption,  
   CWnd* pParentWnd,  
   UINT iSelectPage,  
   HBITMAP hbmWatermark,  
   HPALETTE hpalWatermark = NULL,  
   HBITMAP hbmHeader = NULL   
);  
```  
  
#### Parameters  
 `nIDCaption`  
 ID of the caption to be used for the property sheet.  
  
 `pParentWnd`  
 Points to the parent window of the property sheet. If **NULL**, the parent window will be the main window of the application.  
  
 `iSelectPage`  
 The index of the page that will initially be on top. Default is the first page added to the sheet.  
  
 `pszCaption`  
 Points to a string containing the caption to be used for the property sheet. Cannot be **NULL**.  
  
 `hbmWatermark`  
 A handle to the background bitmap of the property sheet.  
  
 `hpalWatermark`  
 A handle to the palette of the watermark bitmap and/or header bitmap.  
  
 `hbmHeader`  
 A handle to the header bitmap of the property page.  
  
## Remarks  
 To display the property sheet, call [DoModal](../vs140/CPropertySheet--DoModal.md) or [Create](../vs140/CPropertySheet--Create.md). The string contained in the first parameter will be placed in the caption bar for the property sheet.  
  
 If you have multiple parameters (for example, if you are using an array), use [Construct](../vs140/CPropertySheet--Construct.md) instead of `CPropertySheet`.  
  
 You can display watermark and/or header images automatically if you use the third or fourth prototypes of `CPropertySheet`, above, and you pass valid values for the `hbmWatermark`, `hpalWatermark`, and/or `hbmHeader` parameters.  
  
## Example  
 [!CODE [NVC_MFCDocView#131](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#131)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::Construct](../vs140/CPropertySheet--Construct.md)   
 [CPropertySheet::DoModal](../vs140/CPropertySheet--DoModal.md)   
 [CPropertySheet::Create](../vs140/CPropertySheet--Create.md)   
 [CPropertyPage::CPropertyPage](../vs140/CPropertyPage--CPropertyPage.md)