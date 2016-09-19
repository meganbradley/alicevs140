---
title: "CUserTool::DrawToolIcon"
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
ms.assetid: a4906b54-e6e0-4143-9791-f060a7bd8954
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserTool::DrawToolIcon
Draws the user tool icon at the center of a specified rectangle.  
  
## Syntax  
  
```  
void DrawToolIcon(  
   CDC* pDC,  
   const CRect& rectImage   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectImage`  
 Specifies the coordinates of the area to display the icon.  
  
## Requirements  
 **Header:** afxusertool.h  
  
## See Also  
 [CUserTool Class](../vs140/CUserTool-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)