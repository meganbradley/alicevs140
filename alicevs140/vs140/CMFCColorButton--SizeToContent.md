---
title: "CMFCColorButton::SizeToContent"
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
ms.assetid: 5a686f93-50c9-4b92-970b-d109b9b99f0d
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::SizeToContent
Resizes the button control to fit its text and image.  
  
## Syntax  
  
```  
virtual CSize SizeToContent(  
   BOOL bCalcOnly=FALSE   
);  
```  
  
#### Parameters  
 [in] `bCalcOnly`  
 If nonzero, the new size of the button control is calculated but the actual size is not changed.  
  
## Return Value  
 A `CSize` object that specifies a new button control size.  
  
## Remarks  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)