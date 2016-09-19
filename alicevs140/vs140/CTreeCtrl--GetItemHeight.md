---
title: "CTreeCtrl::GetItemHeight"
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
ms.assetid: 4c4e7a6c-5570-4611-88ee-f91729ac8834
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItemHeight
This member function implements the behavior of the Win32 message [TVM_GETITEMHEIGHT](http://msdn.microsoft.com/library/windows/desktop/bb773599), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
SHORT GetItemHeight( ) const;  
  
```  
  
## Return Value  
 The height of the item, in pixels.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#15)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetItemHeight](../vs140/CTreeCtrl--SetItemHeight.md)