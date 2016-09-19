---
title: "CMFCToolBar::GetItemRect"
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
ms.assetid: 71d49a09-dfaf-49d2-9c65-372018d575e8
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetItemRect
Returns the bounding rectangle of the button at a specified index.  
  
## Syntax  
  
```  
virtual void GetItemRect(  
   int nIndex,  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of a toolbar button.  
  
 [out] `lpRect`  
 A pointer to `CRect` object that receives the coordinates of the image bounding rectangle.  
  
## Remarks  
 The `CRect` object to which `lpRect` points is set to 0 if a button at the specified index does not exist.  
  
## Example  
 The following example demonstrates how to use the `GetItemRect` method of the `CMFCToolBar` class. This code snippet is part of the [IE Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_IEDemo#6](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#6)]  
[!CODE [NVC_MFC_IEDemo#9](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#9)]  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)