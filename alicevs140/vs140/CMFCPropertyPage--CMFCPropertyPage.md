---
title: "CMFCPropertyPage::CMFCPropertyPage"
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
ms.assetid: 7ff0bd34-92d4-4072-b5b7-b2ca4bb73775
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyPage::CMFCPropertyPage
Constructs a `CMFCPropertyPage` object.  
  
## Syntax  
  
```  
CMFCPropertyPage(  
   UINT nIDTemplate,  
   UINT nIDCaption=0   
);  
CMFCPropertyPage(  
   LPCTSTR lpszTemplateName,  
   UINT nIDCaption=0   
);  
```  
  
#### Parameters  
 `nIDTemplate`  
 Resource ID of the template for this page.  
  
 `nIDCaption`  
 Resource ID of the label to put in the tab for this page. If 0, the name is obtained from the dialog box template for this page. The default value is 0.  
  
 `lpszTemplateName`  
 Points to the name of the template for this page. Cannot be `NULL`.  
  
## Return Value  
  
## Remarks  
 For more information about the constructor parameters, see [CPropertyPage::CPropertyPage](../vs140/CPropertyPage--CPropertyPage.md).  
  
## Requirements  
 **Header:** afxpropertypage.h  
  
## See Also  
 [CMFCPropertyPage Class](../vs140/CMFCPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertyPage::CPropertyPage](../vs140/CPropertyPage--CPropertyPage.md)