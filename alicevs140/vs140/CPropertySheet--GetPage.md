---
title: "CPropertySheet::GetPage"
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
ms.assetid: 915d4bfd-b19e-469b-a60e-c44382fd2922
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::GetPage
Returns a pointer to the specified page in this property sheet.  
  
## Syntax  
  
```  
  
      CPropertyPage* GetPage(  
   int nPage   
) const;  
```  
  
#### Parameters  
 `nPage`  
 Index of the desired page, starting at 0. Must be between 0 and one less than the number of pages in the property sheet, inclusive.  
  
## Return Value  
 The pointer to the page corresponding to the `nPage` parameter.  
  
## Example  
 See the example for [CPropertyPage::OnWizardFinish](../vs140/CPropertyPage--OnWizardFinish.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::AddPage](../vs140/CPropertySheet--AddPage.md)   
 [CPropertySheet::GetActivePage](../vs140/CPropertySheet--GetActivePage.md)   
 [CPropertySheet::GetPageCount](../vs140/CPropertySheet--GetPageCount.md)   
 [CPropertySheet::RemovePage](../vs140/CPropertySheet--RemovePage.md)   
 [CPropertySheet::SetTitle](../vs140/CPropertySheet--SetTitle.md)   
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)