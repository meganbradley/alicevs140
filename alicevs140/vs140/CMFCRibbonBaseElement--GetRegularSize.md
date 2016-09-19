---
title: "CMFCRibbonBaseElement::GetRegularSize"
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
ms.assetid: 87e34e4e-3a18-4dcf-8342-4aea8b60e61b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::GetRegularSize
Returns the regular size of the ribbon element.  
  
## Syntax  
  
```  
virtual CSize GetRegularSize(  
   CDC* pDC   
) = 0;  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
## Return Value  
 The regular size of the ribbon element.  
  
## Remarks  
  
> [!NOTE]
>  The regular size is the maximal possible size of the ribbon element.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)