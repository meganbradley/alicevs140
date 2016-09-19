---
title: "CMFCPropertyGridProperty::OnKillFocus"
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
ms.assetid: 2c08c597-8177-40b6-a042-f70415319b7e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::OnKillFocus
Called by the framework when the property loses the input focus.  
  
## Syntax  
  
```  
virtual BOOL OnKillFocus(  
   CWnd*    
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `CWnd`|(Not used.) Pointer to a window.|  
  
## Return Value  
 This method always returns `TRUE`.  
  
## Remarks  
 By default, this method does nothing and then returns `TRUE`. If you override this method, return `TRUE` if the framework can end the edit operation when the property loses the input focus.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)