---
title: "COleServerItem::m_sizeExtent"
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
ms.assetid: f2322fd8-e0a8-4870-989f-ec0238ee9c46
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::m_sizeExtent
This member tells the server how much of the object is visible in the container document.  
  
## Syntax  
  
```  
  
CSize m_sizeExtent;  
```  
  
## Remarks  
 The default implementation of [OnSetExtent](../vs140/COleServerItem--OnSetExtent.md) sets this member.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::OnSetExtent](../vs140/COleServerItem--OnSetExtent.md)