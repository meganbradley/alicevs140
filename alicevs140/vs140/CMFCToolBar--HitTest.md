---
title: "CMFCToolBar::HitTest"
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
ms.assetid: 542a5a56-7ffb-45c3-850b-7bb1c4802501
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::HitTest
Returns the index of the toolbar button that is located at the specified position.  
  
## Syntax  
  
```  
virtual int HitTest(  
   CPoint point   
);  
```  
  
#### Parameters  
 [in] `point`  
 The point to be tested, in client coordinates.  
  
## Return Value  
 The index of the button that is located at the specified position, or -1 if there is no such button or the button is a separator.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)