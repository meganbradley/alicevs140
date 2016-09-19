---
title: "CMFCToolBarEditBoxButton::CopyFrom"
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
ms.assetid: cdd04fdd-f61c-4330-9c6d-705f3a4b8b04
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::CopyFrom
Copies the properties of another toolbar button to the current button.  
  
## Syntax  
  
```  
virtual void CopyFrom(  
   const CMFCToolBarButton& src  
);  
```  
  
#### Parameters  
 [in] `src`  
 A reference to the source button from which to copy.  
  
## Remarks  
 Call this method to copy another toolbar button to this toolbar button. `src` must be of type `CMFCToolBarEditBoxButton`.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)