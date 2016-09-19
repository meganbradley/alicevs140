---
title: "CListCtrl::GetCallbackMask"
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
ms.assetid: da54fc6b-3057-44c2-a10d-46779597cf76
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetCallbackMask
Retrieves the callback mask for a list view control.  
  
## Syntax  
  
```  
  
UINT GetCallbackMask( ) const;  
```  
  
## Return Value  
 The list view control's callback mask.  
  
## Remarks  
 A "callback item" is a list view item for which the application — rather than the control — stores the text, icon, or both. Although a list view control can store these attributes for you, you may want to use callback items if your application already maintains some of this information. The callback mask specifies which item state bits are maintained by the application, and it applies to the whole control rather than to a specific item. The callback mask is zero by default, meaning that the control tracks all item states. If an application uses callback items or specifies a nonzero callback mask, it must be able to supply list view item attributes on demand.  
  
## Example  
 See the example for [CListCtrl::SetCallbackMask](../vs140/CListCtrl--SetCallbackMask.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetCallbackMask](../vs140/CListCtrl--SetCallbackMask.md)