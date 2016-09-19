---
title: "CColorDialog::m_cc"
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
ms.assetid: 472c73c0-d411-401b-a0e0-81e28560ab02
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CColorDialog::m_cc
A structure of type [CHOOSECOLOR](http://msdn.microsoft.com/library/windows/desktop/ms646830), whose members store the characteristics and values of the dialog box.  
  
## Syntax  
  
```  
  
CHOOSECOLOR m_cc;  
```  
  
## Remarks  
 After constructing a `CColorDialog` object, you can use `m_cc` to set various aspects of the dialog box before calling the [DoModal](../vs140/CColorDialog--DoModal.md) member function.  
  
## Example  
 [!CODE [NVC_MFCDocView#53](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#53)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CColorDialog Class](../vs140/CColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)