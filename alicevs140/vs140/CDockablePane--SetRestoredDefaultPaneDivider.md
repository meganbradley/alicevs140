---
title: "CDockablePane::SetRestoredDefaultPaneDivider"
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
ms.assetid: ddd4248f-1e81-4275-a2f2-55aa0e9816f6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::SetRestoredDefaultPaneDivider
Sets the restored default pane divider.  
  
## Syntax  
  
```  
void SetRestoredDefaultPaneDivider(  
   HWND hRestoredSlider  
);  
```  
  
#### Parameters  
 [in] `hRestoredSlider`  
 A handle to a pane divider (slider).  
  
## Remarks  
 A restored default pane divider is obtained when a pane is deserialized. For more information, see [CDockablePane::RestoreDefaultPaneDivider](../vs140/CDockablePane--RestoreDefaultPaneDivider.md).  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)