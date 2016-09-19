---
title: "CReBarCtrl::GetRowCount"
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
ms.assetid: fea4fa39-b951-438a-b070-d10b6f000647
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetRowCount
Implements the behavior of the Win32 message [RB_GETROWCOUNT](http://msdn.microsoft.com/library/windows/desktop/bb774471), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
UINT GetRowCount( ) const;  
  
```  
  
## Return Value  
 A **UINT** value that represents the number of band rows in the control.  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#7)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetRowHeight](../vs140/CReBarCtrl--GetRowHeight.md)