---
title: "CMFCPropertySheet::CMFCPropertySheet"
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
ms.assetid: 896d90bc-4731-40ca-8fe2-b13a68d47b56
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertySheet::CMFCPropertySheet
Constructs a `CMFCPropertySheet` object.  
  
## Syntax  
  
```  
CMFCPropertySheet(  
   UINT nIDCaption,  
   CWnd* pParentWnd=NULL,  
   UINT iSelectPage=0   
);  
CMFCPropertySheet(  
   LPCTSTR pszCaption,  
   CWnd* pParentWnd=NULL,  
   UINT iSelectPage=0   
);  
```  
  
#### Parameters  
 [in] `pszCaption`  
 A string that contains the property sheet caption. Cannot be `NULL`.  
  
 [in] `nIDCaption`  
 A resource ID that contains the property sheet caption.  
  
 [in] `pParentWnd`  
 Pointer to the parent window of the property sheet, or `NULL` if the parent window is the main window of the application. The default value is `NULL`.  
  
 [in] `iSelectPage`  
 The zero-based index of the top property page. The default value is 0.  
  
## Remarks  
 For more information, see the parameters for the [CPropertySheet::CPropertySheet](../vs140/CPropertySheet--CPropertySheet.md) constructor.  
  
## Requirements  
 **Header:** afxpropertysheet.h  
  
## See Also  
 [CMFCPropertySheet Class](../vs140/CMFCPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)