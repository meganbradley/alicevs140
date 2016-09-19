---
title: "CMFCColorBar::SetColorName"
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
ms.assetid: bebc5436-a2a4-403b-b257-fae2bb6b096c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::SetColorName
Sets a new name for a specified color.  
  
## Syntax  
  
```  
static void SetColorName(  
   COLORREF color,  
   const CString& strName   
);  
```  
  
#### Parameters  
 [in] `color`  
 The RGB value of a color.  
  
 [in] `strName`  
 The new name for the specified color.  
  
## Remarks  
 This method changes the name of the specified color in all `CMFCColorBar` objects in your application.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)