---
title: "COleControl::DrawMetafile"
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
ms.assetid: 3a90d025-2cea-46fc-a139-7e2eecb796b7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::DrawMetafile
Called by the framework when the metafile device context is being used.  
  
## Syntax  
  
```  
  
      void DrawMetafile(  
   CDC* pDC,  
   CRect& rc  
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to the metafile device context.  
  
 `rc`  
 Rectangular area to be drawn in.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnDraw](../vs140/COleControl--OnDraw.md)   
 [COleControl::DrawContent](../vs140/COleControl--DrawContent.md)   
 [COleControl::OnDrawMetafile](../vs140/COleControl--OnDrawMetafile.md)