---
title: "CRgn::EqualRgn"
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
ms.assetid: 9685ae11-ba8d-4d32-abf8-ee6cfed5c215
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::EqualRgn
Determines whether the given region is equivalent to the region stored in the `CRgn` object.  
  
## Syntax  
  
```  
  
      BOOL EqualRgn(  
   CRgn* pRgn   
) const;  
```  
  
#### Parameters  
 `pRgn`  
 Identifies a region.  
  
## Return Value  
 Nonzero if the two regions are equivalent; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCDocView#150](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#150)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [EqualRgn](http://msdn.microsoft.com/library/windows/desktop/dd162700)