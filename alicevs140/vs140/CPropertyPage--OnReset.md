---
title: "CPropertyPage::OnReset"
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
ms.assetid: 8f1dd48a-2e3d-435d-a98d-47e1e7736af2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnReset
This member function is called by the framework when the user chooses the Cancel button.  
  
## Syntax  
  
```  
  
virtual void OnReset( );  
  
```  
  
## Remarks  
 When the framework calls this function, changes to all property pages that were made by the user previously choosing the Apply Now button are discarded, and the property sheet retains focus.  
  
 Override this member function to specify what action the program takes when the user clicks the Cancel button.  
  
 The default implementation of `OnReset` does nothing.  
  
## Example  
 See the example for [CPropertyPage::OnCancel](../vs140/CPropertyPage--OnCancel.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertyPage::OnCancel](../vs140/CPropertyPage--OnCancel.md)   
 [CPropertyPage::OnApply](../vs140/CPropertyPage--OnApply.md)