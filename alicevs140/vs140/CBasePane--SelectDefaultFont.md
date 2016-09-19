---
title: "CBasePane::SelectDefaultFont"
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
ms.assetid: 81f632b8-618d-4272-86cd-0d9082eee5dc
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::SelectDefaultFont
Selects the default font for a given device context.  
  
## Syntax  
  
```  
CFont* SelectDefaultFont(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A device context.  
  
## Return Value  
 A pointer to the default [CFont Class](../vs140/CFont-Class.md) object.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)