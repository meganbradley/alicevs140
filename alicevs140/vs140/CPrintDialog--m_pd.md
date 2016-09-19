---
title: "CPrintDialog::m_pd"
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
ms.assetid: 2c7ae076-26a4-49ef-b75c-201e08920149
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::m_pd
A structure whose members store the characteristics of the dialog object.  
  
## Syntax  
  
```  
  
PRINTDLG& m_pd;  
```  
  
## Remarks  
 After constructing a `CPrintDialog` object, you can use `m_pd` to set various aspects of the dialog box before calling the [DoModal](../vs140/CPrintDialog--DoModal.md) member function. For more information on the `m_pd` structure, see [PRINTDLG](http://msdn.microsoft.com/library/windows/desktop/ms646843) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 If you modify the `m_pd` data member directly, you will override any default behavior.  
  
## Example  
 [!CODE [NVC_MFCDocView#111](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#111)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)