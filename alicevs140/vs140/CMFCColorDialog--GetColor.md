---
title: "CMFCColorDialog::GetColor"
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
ms.assetid: da0c9357-83f0-4d4e-8812-c07fd710fbd2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorDialog::GetColor
Retrieves the color that the user selects from the color dialog.  
  
## Syntax  
  
```  
COLORREF GetColor() const;  
```  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that contains the RGB information for the color selected in the color dialog box.  
  
## Remarks  
 Call this function after you call the `DoModal` method.  
  
## Requirements  
 **Header:** afxcolordialog.h  
  
## See Also  
 [CMFCColorDialog Class](../vs140/CMFCColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)