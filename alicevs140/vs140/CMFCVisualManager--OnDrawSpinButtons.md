---
title: "CMFCVisualManager::OnDrawSpinButtons"
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
ms.assetid: aaf8274c-4d47-44fd-ab73-f7f2bf0f6fe8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawSpinButtons
The framework calls this method when it draws an instance of the [CMFCSpinButtonCtrl Class](../vs140/CMFCSpinButtonCtrl-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawSpinButtons(  
   CDC* pDC,  
   CRect rectSpin,  
   int nState,  
   BOOL bOrientation,  
   CMFCSpinButtonCtrl* pSpinCtrl  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectSpin`  
 A rectangle that specifies the boundaries of the spin control.  
  
 [in] `nState`  
 A flag that indicates the state of the spin control. See the Remarks section for more information.  
  
 [in] `bOrientation`  
 A Boolean parameter that specifies the orientation of the spin control. A value of `TRUE` indicates the spin control is horizontal. Otherwise, it is vertical.  
  
 [in] `pSpinCtrl`  
 A pointer to a spin control. The framework draws the buttons for this control.  
  
## Remarks  
 The `nState` parameter indicates the state of the spin control. The parameter is one of the following values:  
  
-   AFX_SPIN_PRESSEDUP  
  
-   AFX_SPIN_PRESSEDDOWN  
  
-   AFX_SPIN_HIGHLIGHTEDUP  
  
-   AFX_SPIN_HIGHLIGHTEDDOWN  
  
-   AFX_SPIN_DISABLED  
  
 Override this method in a derived visual manager to customize the appearance of a spin control.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCSpinButtonCtrl Class](../vs140/CMFCSpinButtonCtrl-Class.md)