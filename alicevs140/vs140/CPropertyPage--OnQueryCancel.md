---
title: "CPropertyPage::OnQueryCancel"
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
ms.assetid: db02aaa2-79ad-4ded-b235-8445021da4bc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnQueryCancel
This member function is called by the framework when the user clicks the Cancel button and before the cancel action has taken place.  
  
## Syntax  
  
```  
  
virtual BOOL OnQueryCancel( );  
  
```  
  
## Return Value  
 Returns **FALSE** to prevent the cancel operation or TRUE to allow it.  
  
## Remarks  
 Override this member function to specify an action the program takes when the user clicks the Cancel button.  
  
 The default implementation of `OnQueryCancel` returns **TRUE**.  
  
## Example  
 [!CODE [NVC_MFCDocView#117](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#117)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)