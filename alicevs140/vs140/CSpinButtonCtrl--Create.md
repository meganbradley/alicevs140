---
title: "CSpinButtonCtrl::Create"
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
ms.assetid: 1afdd778-d502-4b5f-a7ec-64e3449c0ff3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSpinButtonCtrl::Create
Creates a spin button control and attaches it to a `CSpinButtonCtrl` object..  
  
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
 Specifies the spin button control's style. Apply any combination of spin button control styles to the control. These styles are described in [Up-Down Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb759885) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `rect`  
 Specifies the spin button control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure  
  
 `pParentWnd`  
 A pointer to the spin button control's parent window, usually a `CDialog`. It must not be **NULL.**  
  
 `nID`  
 Specifies the spin button control's ID.  
  
## Return Value  
 Nonzero if initialization was successful; otherwise 0.  
  
## Remarks  
 You construct a `CSpinButtonCtrl` object in two steps First, call the constructor, and then call **Create**, which creates the spin button control and attaches it to the `CSpinButtonCtrl` object.  
  
 To create a spin button control with extended window styles, call [CSpinButtonCtrl::CreateEx](../vs140/CSpinButtonCtrl--CreateEx.md) instead of **Create**.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSpinButtonCtrl Class](../vs140/CSpinButtonCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSpinButtonCtrl::CSpinButtonCtrl](../vs140/CSpinButtonCtrl--CSpinButtonCtrl.md)