---
title: "CTreeCtrl::SetLineColor"
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
ms.assetid: 4d511173-56df-4080-a3f8-6b41057b0691
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetLineColor
Call this member function to set the current line color for the tree view control.  
  
## Syntax  
  
```  
  
      COLORREF SetLineColor(  
   COLORREF clrNew = CLR_DEFAULT   
);  
```  
  
#### Parameters  
 `clrNew`  
 The new line color.  
  
## Return Value  
 The previous line color.  
  
## Remarks  
 This member function implements the behavior of the win32 message [TVM_SETLINECOLOR](http://msdn.microsoft.com/library/windows/desktop/bb773764), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#35)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetLineColor](../vs140/CTreeCtrl--GetLineColor.md)