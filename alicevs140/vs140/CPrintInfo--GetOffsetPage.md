---
title: "CPrintInfo::GetOffsetPage"
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
ms.assetid: 467ba5c2-e031-4e51-96dd-57e909e0ee23
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::GetOffsetPage
Call this function to retrieve the offset when printing multiple DocObject items from a DocObject client.  
  
## Syntax  
  
```  
  
UINT GetOffsetPage( ) const;  
```  
  
## Return Value  
 The number of pages preceding the first page of a DocObject item being printed in a combined DocObject print job.  
  
## Remarks  
 This value is referenced by the **m_nOffsetPage** member. The first page of your document will be numbered the **m_nOffsetPage** value + 1 when printed as a DocObject with other active documents. The **m_nOffsetPage** member is valid only if the **m_bDocObject** value is **TRUE**.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::m_nOffsetPage](../vs140/CPrintInfo--m_nOffsetPage.md)   
 [CPrintInfo::m_bDocObject](../vs140/CPrintInfo--m_bDocObject.md)