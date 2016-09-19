---
title: "CWnd::GetDescendantWindow"
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
ms.assetid: ba024d0e-df6f-4a0e-a563-e799338abced
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetDescendantWindow
Call this member function to find the descendant window specified by the given ID.  
  
## Syntax  
  
```  
  
      CWnd* GetDescendantWindow(  
   int nID,  
   BOOL bOnlyPerm = FALSE   
) const;  
```  
  
#### Parameters  
 `nID`  
 Specifies the identifier of the control or child window to be retrieved.  
  
 `bOnlyPerm`  
 Specifies whether the window to be returned can be temporary. If **TRUE**, only a permanent window can be returned; if **FALSE,** the function can return a temporary window. For more information on temporary windows see [Technical Note 3](../vs140/TN003--Mapping-of-Windows-Handles-to-Objects.md).  
  
## Return Value  
 A pointer to a `CWnd` object, or **NULL** if no child window is found.  
  
## Remarks  
 This member function searches the entire tree of child windows, not only the windows that are immediate children.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetParentFrame](../vs140/CWnd--GetParentFrame.md)   
 [CWnd::IsChild](../vs140/CWnd--IsChild.md)   
 [CWnd::GetDlgItem](../vs140/CWnd--GetDlgItem.md)