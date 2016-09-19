---
title: "COleControl::ResetVersion"
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
ms.assetid: e77b74e4-c963-4b6b-a992-7e99957cb55a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ResetVersion
Initializes the version number to specified value.  
  
## Syntax  
  
```  
  
      void ResetVersion(  
   DWORD dwVersionDefault   
);  
```  
  
#### Parameters  
 `dwVersionDefault`  
 The version number to be assigned to the control.  
  
## Remarks  
 You can improve a control's binary initialization performance by using `ResetVersion` and `ResetStockProps` to override `COleControl::OnResetState`. See the example at [ResetStockProps](../vs140/COleControl--ResetStockProps.md). For further information on optimizing initialization, see [ActiveX Controls: Optimization](../vs140/MFC-ActiveX-Controls--Optimization.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::ResetStockProps](../vs140/COleControl--ResetStockProps.md)   
 [COleControl::SerializeVersion](../vs140/COleControl--SerializeVersion.md)