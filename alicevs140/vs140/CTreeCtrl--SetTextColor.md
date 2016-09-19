---
title: "CTreeCtrl::SetTextColor"
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
ms.assetid: 3fd22223-d692-4a40-92ac-1fc1e6334be1
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetTextColor
This member function implements the behavior of the Win32 message [TVM_SETTEXTCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb773769), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      COLORREF SetTextColor(  
   COLORREF clr   
);  
```  
  
#### Parameters  
 `clr`  
 A **COLORREF** value that contains the new text color. If this argument is -1, the control will revert to using the system color for the text color.  
  
## Return Value  
 A **COLORREF** value that represents the previous text color. If this value is -1, the control was using the system color for the text color.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#36)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetTextColor](../vs140/CTreeCtrl--GetTextColor.md)