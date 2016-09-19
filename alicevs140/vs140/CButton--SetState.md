---
title: "CButton::SetState"
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
ms.assetid: f8187e26-5906-425b-b566-a55d44944a62
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetState
Sets whether a button control is highlighted or not.  
  
## Syntax  
  
```  
  
      void SetState(  
   BOOL bHighlight   
);  
```  
  
#### Parameters  
 *bHighlight*  
 Specifies whether the button is to be highlighted. A nonzero value highlights the button; a 0 value removes any highlighting.  
  
## Remarks  
 Highlighting affects the exterior of a button control. It has no effect on the check state of a radio button or check box.  
  
 A button control is automatically highlighted when the user clicks and holds the left mouse button. The highlighting is removed when the user releases the mouse button.  
  
## Example  
 [!CODE [NVC_MFC_CButton#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#9)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetState](../vs140/CButton--GetState.md)   
 [CButton::SetCheck](../vs140/CButton--SetCheck.md)   
 [CButton::GetCheck](../vs140/CButton--GetCheck.md)   
 [BM_SETSTATE](http://msdn.microsoft.com/library/windows/desktop/bb761823)