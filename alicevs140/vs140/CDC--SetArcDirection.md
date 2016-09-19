---
title: "CDC::SetArcDirection"
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
ms.assetid: 52684208-cf55-490a-8ded-c2be64b19b5a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetArcDirection
Sets the drawing direction to be used for arc and rectangle functions.  
  
## Syntax  
  
```  
  
      int SetArcDirection(  
   int nArcDirection   
);  
```  
  
#### Parameters  
 *nArcDirection*  
 Specifies the new arc direction. This parameter can be either of the following values:  
  
-   **AD_COUNTERCLOCKWISE** Figures drawn counterclockwise.  
  
-   **AD_CLOCKWISE** Figures drawn clockwise.  
  
## Return Value  
 Specifies the old arc direction, if successful; otherwise 0.  
  
## Remarks  
 The default direction is counterclockwise. The `SetArcDirection` function specifies the direction in which the following functions draw:  
  
|Arc|Pie|  
|---------|---------|  
|`ArcTo`|**Rectangle**|  
|`Chord`|`RoundRect`|  
|**Ellipse**||  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetArcDirection](../vs140/CDC--GetArcDirection.md)   
 [SetArcDirection](http://msdn.microsoft.com/library/windows/desktop/dd162961)