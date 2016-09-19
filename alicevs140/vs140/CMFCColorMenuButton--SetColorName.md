---
title: "CMFCColorMenuButton::SetColorName"
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
ms.assetid: 0fb23857-153c-4097-bf92-1ece63254e8c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorMenuButton::SetColorName
Sets a new name for the specified color.  
  
## Syntax  
  
```  
static void SetColorName(  
   COLORREF color,  
   const CString& strName   
);  
```  
  
#### Parameters  
 [in] `color`  
 The RGB value of the color whose name changes.  
  
 [in] `strName`  
 The new name of the color.  
  
## Remarks  
  
## Requirements  
 **Header:** afxcolormenubutton.h  
  
## See Also  
 [CMFCColorMenuButton Class](../vs140/CMFCColorMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)