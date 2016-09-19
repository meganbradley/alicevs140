---
title: "CPropertyPage::OnSetActive"
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
ms.assetid: 46ead56c-2454-4af3-9b9f-8eaac9f861ff
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnSetActive
This member function is called by the framework when the page is chosen by the user and becomes the active page.  
  
## Syntax  
  
```  
  
virtual BOOL OnSetActive( );  
```  
  
## Return Value  
 Nonzero if the page was successfully set active; otherwise 0.  
  
## Remarks  
 Override this member function to perform tasks when a page is activated. Your override of this member function would typically call the default version after updating data members, to allow it to update the page controls with the new data.  
  
 The default implementation creates the window for the page, if not previously created, and makes it the active page.  
  
## Example  
 See the example for [CPropertySheet::SetFinishText](../vs140/CPropertySheet--SetFinishText.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertyPage::OnKillActive](../vs140/CPropertyPage--OnKillActive.md)