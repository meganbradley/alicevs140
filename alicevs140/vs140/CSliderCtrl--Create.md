---
title: "CSliderCtrl::Create"
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
ms.assetid: 3702e571-2d57-4b8e-aaad-7d070d7afca0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::Create
Creates a slider control and attaches it to a `CSliderCtrl` object.  
  
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
 `dwStyle`  
 Specifies the slider control's style. Apply any combination of [slider control styles](http://msdn.microsoft.com/library/windows/desktop/bb760147), described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)], to the control.  
  
 `rect`  
 Specifies the slider control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
 `pParentWnd`  
 Specifies the slider control's parent window, usually a `CDialog`. It must not be **NULL**.  
  
 `nID`  
 Specifies the slider control's ID.  
  
## Return Value  
 Nonzero if initialization was successful; otherwise 0.  
  
## Remarks  
 You construct a `CSliderCtrl` in two steps. First, call the constructor, and then call **Create**, which creates the slider control and attaches it to the `CSliderCtrl` object.  
  
 Depending on the values set for `dwStyle`, the slider control can have either a vertical or horizontal orientation. It can have tick marks on either side, both sides, or neither. It can also be used to specify a range of consecutive values.  
  
 To apply extended window styles to the slider control, call [CreateEx](../vs140/CSliderCtrl--CreateEx.md) instead of **Create**.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::CSliderCtrl](../vs140/CSliderCtrl--CSliderCtrl.md)