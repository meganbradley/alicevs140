---
title: "CMFCLinkCtrl::SizeToContent"
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
ms.assetid: 43b2b558-f690-4cb6-bcb1-91acf9ee081f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCLinkCtrl::SizeToContent
Resizes the button to contain the button text or bitmap.  
  
## Syntax  
  
```  
virtual CSize SizeToContent(  
   BOOL bVCenter=FALSE,  
   BOOL bHCenter=FALSE   
);  
```  
  
#### Parameters  
 [in] `bVCenter`  
 `TRUE` to center the button text and bitmap vertically between the top and bottom of the link control; otherwise, `FALSE`. The default value is `FALSE`.  
  
 [in] `bHCenter`  
 `TRUE` to center the button text and bitmap horizontally between the left and right sides of the link control; otherwise, `FALSE`. The default value is `FALSE`.  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object that contains the new size of the link control.  
  
## Remarks  
  
## Requirements  
 **Header:** afxlinkctrl.h  
  
## See Also  
 [CMFCLinkCtrl Class](../vs140/CMFCLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)