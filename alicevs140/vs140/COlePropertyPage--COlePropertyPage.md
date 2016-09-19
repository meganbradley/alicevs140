---
title: "COlePropertyPage::COlePropertyPage"
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
ms.assetid: 007a2f50-f19b-4d01-9982-05d41db840d9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::COlePropertyPage
Constructs a `COlePropertyPage` object.  
  
## Syntax  
  
```  
  
      COlePropertyPage(  
   UINT idDlg,  
   UINT idCaption   
);  
```  
  
#### Parameters  
 *idDlg*  
 Resource ID of the dialog template.  
  
 *idCaption*  
 Resource ID of the property page's caption.  
  
## Remarks  
 When you implement a subclass of `COlePropertyPage`, your subclass's constructor should use the `COlePropertyPage` constructor to identify the dialog-template resource on which the property page is based and the string resource containing its caption.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)