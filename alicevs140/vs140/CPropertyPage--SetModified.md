---
title: "CPropertyPage::SetModified"
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
ms.assetid: ba484fb6-968e-4e66-beeb-7a5179d25dd9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::SetModified
Call this member function to enable or disable the Apply Now button, based on whether the settings in the property page should be applied to the appropriate external object.  
  
## Syntax  
  
```  
  
      void SetModified(  
   BOOL bChanged = TRUE   
);  
```  
  
#### Parameters  
 `bChanged`  
 **TRUE** to indicate that the property page settings have been modified since the last time they were applied; **FALSE** to indicate that the property page settings have been applied, or should be ignored.  
  
## Remarks  
 The framework keeps track of which pages are "dirty," that is, property pages for which you have called **SetModified( TRUE )**. The Apply Now button will always be enabled if you call **SetModified( TRUE )** for one of the pages. The Apply Now button will be disabled when you call **SetModified( FALSE )** for one of the pages, but only if none of the other pages is "dirty."  
  
## Example  
 [!CODE [NVC_MFCDocView#127](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#127)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertyPage::CancelToClose](../vs140/CPropertyPage--CancelToClose.md)