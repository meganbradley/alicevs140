---
title: "CMFCRibbonButtonsGroup::GetButton"
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
ms.assetid: d5821e23-2315-4ab3-91c8-0888dd327b89
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButtonsGroup::GetButton
Returns a pointer to the button that is located at a specified index.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* GetButton(  
   int i   
) const;  
```  
  
#### Parameters  
 [in] `i`  
 A zero-based index of a button to return.  
  
## Return Value  
 A pointer to the button that is located at the specified index. `NULL` if the specified index is out of range.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbuttonsgroup.h  
  
## See Also  
 [CMFCRibbonButtonsGroup Class](../vs140/CMFCRibbonButtonsGroup-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)