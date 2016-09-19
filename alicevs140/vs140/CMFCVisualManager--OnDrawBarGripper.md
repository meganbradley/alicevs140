---
title: "CMFCVisualManager::OnDrawBarGripper"
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
ms.assetid: f1438c11-aa70-4f05-9294-511a21ff4881
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawBarGripper
Called by the framework when it draws the gripper for a control bar.  
  
## Syntax  
  
```  
virtual void OnDrawBarGripper(  
   CDC* pDC,  
   CRect rectGripper,  
   BOOL bHorz,  
   CBasePane* pBar   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context for a control bar.  
  
 [in] `rectGripper`  
 The bounding rectangle for the control bar.  
  
 [in] `bHorz`  
 A Boolean parameter that specifies whether the control bar is docked horizontally or vertically.  
  
 [in] `pBar`  
 A pointer to a control bar. The visual manager draws the gripper of this control bar.  
  
## Remarks  
 The default implementation of this method displays the standard gripper. To customize the appearance of the gripper, override this method in a custom class derived from the [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md).  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)