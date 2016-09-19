---
title: "CTreeCtrl::GetLineColor"
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
ms.assetid: 044a269b-7856-4451-9fde-9a09f250547a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetLineColor
This member function implements the behavior of the win32 message [TVM_GETLINECOLOR](http://msdn.microsoft.com/library/windows/desktop/bb773619), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
COLORREF GetLineColor( ) const;  
  
```  
  
## Return Value  
 The current line color.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#19)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetLineColor](../vs140/CTreeCtrl--SetLineColor.md)