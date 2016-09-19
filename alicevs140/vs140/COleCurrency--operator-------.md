---
title: "COleCurrency::operator &lt;&lt;, &gt;&gt;"
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
ms.assetid: 47f12021-25a0-4652-9d35-7c524b1d73c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::operator &lt;&lt;, &gt;&gt;
Supports diagnostic dumping and storing to an archive.  
  
## Syntax  
  
```  
  
      friend CDumpContext& operator <<(  
   CDumpContext& dc,  
   COleCurrency curSrc   
);  
friend CArchive& operator <<(  
   CArchive& ar,  
   COleCurrency curSrc   
);  
friend CArchive& operator >>(  
   CArchive& ar,  
   COleCurrency& curSrc   
);  
```  
  
## Remarks  
 The extraction (**>>**) operator supports loading from an archive.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDumpContext Class](../vs140/CDumpContext-Class.md)   
 [CArchive Class](../vs140/CArchive-Class.md)