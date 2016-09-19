---
title: "CMFCVisualManager::OnDrawMenuSystemButton"
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
ms.assetid: 04f59258-eb89-4efb-b4a3-8df2bfaa32f4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawMenuSystemButton
The framework calls this method when it draws a menu system button for the application.  
  
## Syntax  
  
```  
virtual void OnDrawMenuSystemButton(  
   CDC* pDC,  
   CRect rect,  
   UINT uiSystemCommand,  
   UINT nStyle,  
   BOOL bHighlight   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the button.  
  
 [in] `uiSystemCommand`  
 A flag that specifies which system command is associated with the button. Possible values are SC_CLOSE, SC_MINIMIZE, and SC_RESTORE.  
  
 [in] `nStyle`  
 A flag that specifies the current style of the button. Possible values are TBBS_PRESSED, TBBS_DISABLED, and 0.  
  
 [in] `bHighlight`  
 A Boolean parameter that specifies whether the button is highlighted.  
  
## Remarks  
 The menu system buttons are the **Close**, **Minimize**, **Maximize**, and **Restore** buttons located on the title bar.  
  
 The default implementation for this method calls [CDC::DrawFrameControl](../vs140/CDC--DrawFrameControl.md) with the `DFC_CAPTION` type. Override this method in your derived visual manager class to customize the appearance of system buttons.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)