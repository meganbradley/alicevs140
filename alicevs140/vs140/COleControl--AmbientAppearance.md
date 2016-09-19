---
title: "COleControl::AmbientAppearance"
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
ms.assetid: 54ee38bb-0a7c-4a03-9577-215481ce0c12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientAppearance
Retrieves the current appearance setting for the control object.  
  
## Syntax  
  
```  
  
short AmbientAppearance( );  
  
```  
  
## Return Value  
 The appearance of the control:  
  
-   **0** Flat appearance  
  
-   **1** 3D appearance  
  
## Remarks  
 Call this function to retrieve the current value of the **DISPID_AMBIENT_APPEARANCE** property for the control.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)