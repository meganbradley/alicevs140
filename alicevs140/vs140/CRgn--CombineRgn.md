---
title: "CRgn::CombineRgn"
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
ms.assetid: c20ff366-845d-465c-9fff-69205aceec51
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CombineRgn
Creates a new GDI region by combining two existing regions.  
  
## Syntax  
  
```  
  
      int CombineRgn(  
   CRgn* pRgn1,  
   CRgn* pRgn2,  
   int nCombineMode   
);  
```  
  
#### Parameters  
 `pRgn1`  
 Identifies an existing region.  
  
 `pRgn2`  
 Identifies an existing region.  
  
 `nCombineMode`  
 Specifies the operation to be performed when combining the two source regions. It can be any one of the following values:  
  
-   **RGN_AND** Uses overlapping areas of both regions (intersection).  
  
-   **RGN_COPY** Creates a copy of region 1 (identified by `pRgn1`).  
  
-   **RGN_DIFF** Creates a region consisting of the areas of region 1 (identified by `pRgn1`) that are not part of region 2 (identified by `pRgn2`).  
  
-   **RGN_OR** Combines both regions in their entirety (union).  
  
-   **RGN_XOR** Combines both regions but removes overlapping areas.  
  
## Return Value  
 Specifies the type of the resulting region. It can be one of the following values:  
  
-   **COMPLEXREGION** New region has overlapping borders.  
  
-   **ERROR** No new region created.  
  
-   **NULLREGION** New region is empty.  
  
-   **SIMPLEREGION** New region has no overlapping borders.  
  
## Remarks  
 The regions are combined as specified by `nCombineMode`.  
  
 The two specified regions are combined, and the resulting region handle is stored in the `CRgn` object. Thus, whatever region is stored in the `CRgn` object is replaced by the combined region.  
  
 The size of a region is limited to 32,767 by 32,767 logical units or 64K of memory, whichever is smaller.  
  
 Use [CopyRgn](../vs140/CRgn--CopyRgn.md) to simply copy one region into another region.  
  
## Example  
 [!CODE [NVC_MFCDocView#144](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#144)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRgn::CopyRgn](../vs140/CRgn--CopyRgn.md)   
 [CombineRgn](http://msdn.microsoft.com/library/windows/desktop/dd183465)