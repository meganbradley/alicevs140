---
title: "COleControl::SetInitialSize"
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
ms.assetid: 167fa13f-4ae3-43b7-b7bc-a6b69965cf3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetInitialSize
Sets the size of an OLE control when first displayed in a container.  
  
## Syntax  
  
```  
  
      void SetInitialSize(  
   int cx,  
   int cy   
);  
```  
  
#### Parameters  
 `cx`  
 The initial width of the OLE control in pixels.  
  
 `cy`  
 The initial height of the OLE control in pixels.  
  
## Remarks  
 Call this function in your constructor to set the initial size of your control. The initial size is measured in device units, or pixels. It is recommended that this call be made in your control's constructor.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)