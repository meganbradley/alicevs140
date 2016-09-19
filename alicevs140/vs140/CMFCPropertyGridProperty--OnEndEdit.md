---
title: "CMFCPropertyGridProperty::OnEndEdit"
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
ms.assetid: 5b45b313-58fb-491e-8b57-2f6301ae50a3
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::OnEndEdit
Called by the framework when the user is finished modifying a property value.  
  
## Syntax  
  
```  
virtual BOOL OnEndEdit();  
```  
  
## Return Value  
 This method always returns `TRUE`.  
  
## Remarks  
 By default, this method destroys the current editing control and then returns `TRUE`.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)