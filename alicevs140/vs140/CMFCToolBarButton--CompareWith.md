---
title: "CMFCToolBarButton::CompareWith"
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
ms.assetid: d0f9464c-0f5d-4408-b3e1-0205e92b41db
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::CompareWith
Compares this instance with the provided `CMFCToolBarButton` object.  
  
## Syntax  
  
```  
virtual BOOL CompareWith(  
   const CMFCToolBarButton& other  
) const;  
```  
  
#### Parameters  
 [in] `other`  
 Reference to the object to compare with this instance.  
  
## Return Value  
 Nonzero if the provided object equals the value of this instance; otherwise, 0.  
  
## Remarks  
 The default implementation determines whether the command ID of the provided object equals the command ID of this instance. Override this method if you must perform additional processing to determine whether two `CMFCToolBarButton` objects are equal.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)