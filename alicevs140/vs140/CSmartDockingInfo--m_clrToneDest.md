---
title: "CSmartDockingInfo::m_clrToneDest"
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
ms.assetid: 1bbce36a-0996-47f1-b05d-56cac1a934e3
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSmartDockingInfo::m_clrToneDest
Specifies the color that will replace `m_clrToneSrc` in smart docking marker bitmaps.  
  
## Syntax  
  
```  
COLORREF m_clrToneDest;  
```  
  
## Remarks  
 Set this value to change the color of marker bitmaps programmatically. For example, if you want to change the color of the standard markers provided with the framework, set this value to the desired color. By default, [CSmartDockingInfo::m_clrToneSrc](../vs140/CSmartDockingInfo--m_clrToneSrc.md) is set to RGB (61, 123, 241) (a bluish color).  
  
 To change the color of custom markers, you must specify both `m_clrToneDest` and `m_clrToneSrc`.  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CSmartDockingInfo Class](../vs140/CSmartDockingInfo-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)