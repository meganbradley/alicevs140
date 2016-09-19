---
title: "CTreeCtrl::GetInsertMarkColor"
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
ms.assetid: 7a9f51cd-51b7-4923-8600-616b2590f556
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetInsertMarkColor
This member function implements the behavior of the Win32 message [TVM_GETINSERTMARKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb773590), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
COLORREF GetInsertMarkColor( ) const;  
  
```  
  
## Return Value  
 A **COLORREF** value that contains the current insertion mark color.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#13)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetInsertMarkColor](../vs140/CTreeCtrl--SetInsertMarkColor.md)