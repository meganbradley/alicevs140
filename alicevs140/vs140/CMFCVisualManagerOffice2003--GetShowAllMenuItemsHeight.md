---
title: "CMFCVisualManagerOffice2003::GetShowAllMenuItemsHeight"
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
ms.assetid: e500a58d-46ff-4033-8658-f702b3305689
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::GetShowAllMenuItemsHeight
Returns the height of all menu items.  
  
## Syntax  
  
```  
virtual int GetShowAllMenuItemsHeight(  
   CDC* pDC,  
   const CSize& sizeDefault  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context.  
  
 [in] `sizeDefault`  
 Default menu size.  
  
## Return Value  
 By default, returns the height of all menu images plus margins.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)