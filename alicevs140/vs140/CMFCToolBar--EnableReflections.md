---
title: "CMFCToolBar::EnableReflections"
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
ms.assetid: 963dbe1a-4387-4c4d-b656-7c70ed415150
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::EnableReflections
Enables or disables command reflection.  
  
## Syntax  
  
```  
void EnableReflections(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable command reflection; `FALSE` to disable command reflection.  
  
## Remarks  
 Call this method to enable command reflection for toolbar buttons that contain embedded controls, such as combo boxes.  
  
 For more information about command reflection, see [TN062: Message Reflection for Windows Controls](../vs140/TN062--Message-Reflection-for-Windows-Controls.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [TN062: Message Reflection for Windows Controls](../vs140/TN062--Message-Reflection-for-Windows-Controls.md)