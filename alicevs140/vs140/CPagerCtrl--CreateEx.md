---
title: "CPagerCtrl::CreateEx"
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
ms.assetid: 16903d15-461d-4e48-926a-3c2ff49fca1a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::CreateEx
Creates a pager control with specified extended styles and attaches it to the current `CPagerCtrl` object.  
  
## Syntax  
  
```  
virtual BOOL CreateEx(  
        DWORD dwExStyle,   
        DWORD dwStyle,   
        const RECT& rect,   
        CWnd* pParentWnd,   
        UINT nID  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwExStyle`|A bitwise combination of extended styles to be applied to the control. For more information, see the `dwExStyle` parameter of the [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) function.|  
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
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Pager Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb760859)   
 [Window Styles](../vs140/Window-Styles.md)