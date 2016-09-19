---
title: "CPagerCtrl::Create"
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
ms.assetid: a366f2c9-8705-4f16-9726-a49328220182
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::Create
Creates a pager control with specified styles and attaches it to the current `CPagerCtrl` object.  
  
## Syntax  
  
```  
virtual BOOL Create(  
        DWORD dwStyle,   
        const RECT& rect,   
        CWnd* pParentWnd,   
        UINT nID  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwStyle`|A bitwise combination (OR) of [window styles](../vs140/Window-Styles.md) and [pager control styles](http://msdn.microsoft.com/library/windows/desktop/bb760859) to be applied to the control.|  
|[in] `rect`|A reference to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that contains the position and size of the control in client coordinates.|  
|[in] `pParentWnd`|A pointer to a [CWnd](../vs140/CWnd-Class.md) object that is the parent window of the control. This parameter cannot be `NULL`.|  
|[in] `nID`|The ID of the control.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Remarks  
 To create a pager control, declare a `CPagerCtrl` variable, then call the [CPagerCtrl::Create](../vs140/CPagerCtrl--Create.md) or [CPagerCtrl::CreateEx](../vs140/CPagerCtrl--CreateEx.md) method on that variable.  
  
## Example  
 The following example creates a pager control, then uses the [CPagerCtrl::SetChild](../vs140/CPagerCtrl--SetChild.md) method to associate a very long button control with the pager control. The example then uses the [CPagerCtrl::SetButtonSize](../vs140/CPagerCtrl--SetButtonSize.md) method to set the height of the pager control to 20 pixels, and the [CPagerCtrl::SetBorder](../vs140/CPagerCtrl--SetBorder.md) method to set the border thickness to 1 pixel.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#1)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Pager Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb760859)   
 [Window Styles](../vs140/Window-Styles.md)