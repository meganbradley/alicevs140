---
title: "CMFCDropDownToolbarButton::CopyFrom"
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
ms.assetid: bb8318fa-76c0-440f-93c8-51cb690b21c8
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::CopyFrom
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
 Call this method to copy another toolbar button to this toolbar button. `src` must be of type `CMFCDropDownToolbarButton`.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)