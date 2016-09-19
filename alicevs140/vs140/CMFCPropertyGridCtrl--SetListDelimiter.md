---
title: "CMFCPropertyGridCtrl::SetListDelimiter"
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
ms.assetid: ea61d199-5290-401d-8a7b-7568a972a927
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::SetListDelimiter
Defines a character that is used as a delimiter in a list of property values.  
  
## Syntax  
  
```  
void SetListDelimiter(  
   TCHAR c   
);  
```  
  
#### Parameters  
 [in] `c`  
 A character to serve as a delimiter.  
  
## Remarks  
 Use this method to define a delimiter character in a list of property values that are used in the [CMFCPropertyGridProperty::CMFCPropertyGridProperty](../vs140/CMFCPropertyGridProperty--CMFCPropertyGridProperty.md) constructor. In that constructor, set the `bIsValueList` parameter to `TRUE`.  
  
 By default, the [CMFCPropertyGridCtrl::CMFCPropertyGridCtrl](../vs140/CMFCPropertyGridCtrl--CMFCPropertyGridCtrl.md) constructor sets the delimiter character to comma (',').  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridCtrl::CMFCPropertyGridCtrl](../vs140/CMFCPropertyGridCtrl--CMFCPropertyGridCtrl.md)   
 [CMFCPropertyGridProperty::CMFCPropertyGridProperty](../vs140/CMFCPropertyGridProperty--CMFCPropertyGridProperty.md)