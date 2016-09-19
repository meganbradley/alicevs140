---
title: "CPropertyPage::CancelToClose"
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
ms.assetid: 81fac40b-c7fc-4b07-b9ba-b854bf9e8155
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::CancelToClose
Call this function after an unrecoverable change has been made to the data in a page of a modal property sheet.  
  
## Syntax  
  
```  
  
void CancelToClose( );  
```  
  
## Remarks  
 This function will change the OK button to Close and disable the Cancel button. This change alerts the user that a change is permanent and the modifications cannot be cancelled.  
  
 The `CancelToClose` member function does nothing in a modeless property sheet, because a modeless property sheet does not have a Cancel button by default.  
  
## Example  
 See the example for [CPropertyPage::QuerySiblings](../vs140/CPropertyPage--QuerySiblings.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertyPage::OnKillActive](../vs140/CPropertyPage--OnKillActive.md)   
 [CPropertyPage::SetModified](../vs140/CPropertyPage--SetModified.md)