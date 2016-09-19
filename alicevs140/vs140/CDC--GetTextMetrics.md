---
title: "CDC::GetTextMetrics"
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
ms.assetid: 1e0db5a0-2277-4abb-9de5-c48ea52cff2f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetTextMetrics
Retrieves the metrics for the current font using the attribute device context.  
  
## Syntax  
  
```  
  
      BOOL GetTextMetrics(  
   LPTEXTMETRIC lpMetrics   
) const;  
```  
  
#### Parameters  
 `lpMetrics`  
 Points to the [TEXTMETRIC](http://msdn.microsoft.com/library/windows/desktop/dd145132) structure that receives the metrics.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetTextAlign](../vs140/CDC--GetTextAlign.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)   
 [CDC::GetOutputTextMetrics](../vs140/CDC--GetOutputTextMetrics.md)   
 [CDC::GetTextExtent](../vs140/CDC--GetTextExtent.md)   
 [CDC::GetTextFace](../vs140/CDC--GetTextFace.md)   
 [CDC::SetTextJustification](../vs140/CDC--SetTextJustification.md)   
 [GetTextMetrics](http://msdn.microsoft.com/library/windows/desktop/dd144941)