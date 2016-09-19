---
title: "CMFCColorDialog::GetPalette"
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
ms.assetid: 1321f052-1825-4064-9ed3-9b4e89af2669
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorDialog::GetPalette
Retrieves the color palette that is available in the current color dialog.  
  
## Syntax  
  
```  
CPalette* GetPalette() const;  
```  
  
## Return Value  
 A pointer to the `CPalette` object that was specified in the `CMFCColorDialog` constructor.  
  
## Remarks  
 The color palette specifies the colors that the user can choose.  
  
## Requirements  
 **Header:** afxcolordialog.h  
  
## See Also  
 [CMFCColorDialog Class](../vs140/CMFCColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)