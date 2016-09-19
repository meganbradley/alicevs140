---
title: "CDockingManager::SetSmartDockingParams"
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
ms.assetid: 3f9bfbeb-995c-44be-bd53-0cd12abc63b2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::SetSmartDockingParams
Sets the parameters that define the behavior of smart docking.  
  
## Syntax  
  
```  
static void SetSmartDockingParams(  
    CSmartDockingInfo& params  
);  
```  
  
#### Parameters  
 [in, out] `params`  
 Defines the parameters for smart docking.  
  
## Remarks  
 Call this method if you want to customize the appearance, color, or shape of the smart docking markers.  
  
 To use the default look for smart docking markers, pass an uninitialized instance of [CSmartDockingInfo Class](../vs140/CSmartDockingInfo-Class.md) to `params`.  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)