---
title: "CHeaderCtrl::SetHotDivider"
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
ms.assetid: 0b4a29bb-def2-4570-a834-b2e5f49664ea
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::SetHotDivider
Changes the divider between header items to indicate a manual drag and drop of a header item.  
  
## Syntax  
  
```  
  
      int SetHotDivider(  
   CPoint pt   
);  
int SetHotDivider(  
   int nIndex   
);  
```  
  
#### Parameters  
 `pt`  
 The position of the pointer. The header control highlights the appropriate divider based on the pointer's position.  
  
 `nIndex`  
 The index of the highlighted divider.  
  
## Return Value  
 The index of the highlighted divider.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [HDM_SETHOTDIVIDER](http://msdn.microsoft.com/library/windows/desktop/bb775363), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. It is provided to support header item drag and drop.  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#16)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)