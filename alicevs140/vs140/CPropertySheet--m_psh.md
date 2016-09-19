---
title: "CPropertySheet::m_psh"
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
ms.assetid: 52eb4a50-6d27-432d-a946-2b7911b2185e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::m_psh
A structure whose members store the characteristics of [PROPSHEETHEADER](http://msdn.microsoft.com/library/windows/desktop/bb774546).  
  
## Remarks  
 Use this structure to initialize the appearance of the property sheet after it is constructed but before it is displayed with the [DoModal](../vs140/CPropertySheet--DoModal.md) member function. For example, set the `dwSize` member of `m_psh` to the size you want the property sheet to have.  
  
 For more information on this structure, including a listing of its members, see **PROPSHEETHEADER** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#143](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#143)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::DoModal](../vs140/CPropertySheet--DoModal.md)