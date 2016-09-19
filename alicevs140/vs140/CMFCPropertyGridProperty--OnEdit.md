---
title: "CMFCPropertyGridProperty::OnEdit"
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
ms.assetid: 35ead7c0-fed3-4f09-8fbd-f81c0d7e00ff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::OnEdit
Called by the framework when the user is about to modify a property value.  
  
## Syntax  
  
```  
virtual BOOL OnEdit(  
   LPPOINT lptClick   
);  
```  
  
#### Parameters  
 [in] `lptClick`  
 (This parameter is not used.) A pointer to a point, in client coordinates.  
  
## Return Value  
 `TRUE` if the edit operation starts successfully; otherwise, `FALSE`.  
  
## Remarks  
 This function is called by the framework when the user is about to modify a property value. By default, this method starts the appropriate editor for a combo box control or a spin control.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)