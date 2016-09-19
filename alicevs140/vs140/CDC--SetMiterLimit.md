---
title: "CDC::SetMiterLimit"
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
ms.assetid: 3626c99f-6fb7-446a-b91a-9b01542bf5cc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetMiterLimit
Sets the limit for the length of miter joins for the device context.  
  
## Syntax  
  
```  
  
      BOOL SetMiterLimit(  
   float fMiterLimit   
);  
```  
  
#### Parameters  
 *fMiterLimit*  
 Specifies the new miter limit for the device context.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The miter length is defined as the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls on the outside of the join. The miter limit is the maximum allowed ratio of the miter length to the line width. The default miter limit is 10.0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetMiterLimit](../vs140/CDC--GetMiterLimit.md)   
 [SetMiterLimit](http://msdn.microsoft.com/library/windows/desktop/dd145076)