---
title: "CMFCButton::SizeToContent"
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
ms.assetid: 2f15f415-c78c-437c-a761-166c42d48f9a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::SizeToContent
Resizes a button to contain its button text and image.  
  
## Syntax  
  
```  
virtual CSize SizeToContent(  
   BOOL bCalcOnly=FALSE   
);  
```  
  
#### Parameters  
 [in] `bCalcOnly`  
 `TRUE` to calculate, but not change, the new size of the button; `FALSE` to change the size of the button. The default is `FALSE`.  
  
## Return Value  
 A `CSize` object that contains the new size of the button.  
  
## Remarks  
 By default, this method calculates a new size that includes a horizontal margin of 10 pixels and a vertical margin of 5 pixels.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)