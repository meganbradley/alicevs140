---
title: "CRgn::CreateFromData"
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
ms.assetid: bde6e1b7-c7b2-458c-9f2b-d00956dd32d1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CreateFromData
Creates a region from the given region and transformation data.  
  
## Syntax  
  
```  
  
      BOOL CreateFromData(  
   const XFORM* lpXForm,  
   int nCount,  
   const RGNDATA* pRgnData   
);  
```  
  
#### Parameters  
 *lpXForm*  
 Points to an [XFORM](../vs140/XFORM-Structure.md) data structure that defines the transformation to be performed on the region. If this pointer is **NULL**, the identity transformation is used.  
  
 `nCount`  
 Specifies the number of bytes pointed to by `pRgnData`.  
  
 `pRgnData`  
 Points to a [RGNDATA](../vs140/RGNDATA-Structure.md) data structure that contains the region data.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 An application can retrieve data for a region by calling the `CRgn::GetRegionData` function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRgn::GetRegionData](../vs140/CRgn--GetRegionData.md)   
 [ExtCreateRegion](http://msdn.microsoft.com/library/windows/desktop/dd162706)