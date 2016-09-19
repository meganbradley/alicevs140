---
title: "COleIPFrameWndEx::GetTearOffBars"
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
ms.assetid: a7d1e4b9-921b-4c1d-912d-0eb2f933f959
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::GetTearOffBars
Returns a list of pane objects that are in a tear-off state.  
  
## Syntax  
  
```  
const CObList& GetTearOffBars() const;  
```  
  
## Return Value  
 A reference to a `CObList` object that contains a collection of pointers to the [CBasePane Class](../vs140/CBasePane-Class.md)-derived objects.  
  
## Remarks  
 The `COleIPFrameWndEx` object maintains the collection of tear-off menus as a list of [CBasePane Class](../vs140/CBasePane-Class.md)-derived objects. Use this method to retrieve a reference to this list.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)