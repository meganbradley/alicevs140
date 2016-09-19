---
title: "COleControl::ClipCaretRect"
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
ms.assetid: 6b7cda3e-e21f-4f46-ae9f-378ea3149b0f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ClipCaretRect
Adjusts a caret rectangle if it is entirely or partially covered by overlapping, opaque objects.  
  
## Syntax  
  
```  
  
      BOOL ClipCaretRect(  
   LPRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 On input, a pointer to a [RECT](../vs140/RECT-Structure.md) structure that contains the caret area to be adjusted. On output, the adjusted caret area, or **NULL** if the caret rectangle is completely covered.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 A caret is a flashing line, block, or bitmap that typically indicates where text or graphics will be inserted.  
  
 A windowless object cannot safely show a caret without first checking whether the caret is partially or totally hidden by overlapping objects. In order to make that possible, an object can use `ClipCaretRect` to get the caret adjusted (reduced) to ensure it fits in the clipping region.  
  
 Objects creating a caret should submit the caret rectangle to `ClipCaretRect` and use the adjusted rectangle for the caret. If the caret is entirely hidden, this method will return **FALSE** and the caret should not be shown at all in this case.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)