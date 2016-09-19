---
title: "CToolBar::GetItemRect"
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
ms.assetid: 865bed6a-3520-47b9-8902-da9daa7f5df9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::GetItemRect
This member function fills the `RECT` structure whose address is contained in `lpRect` with the coordinates of the button or separator specified by `nIndex`.  
  
## Syntax  
  
```  
  
      virtual void GetItemRect(  
   int nIndex,  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Index of the item (button or separator) whose rectangle coordinates are to be retrieved.  
  
 `lpRect`  
 Address of the [RECT](../vs140/RECT-Structure.md) structure that will contain the item's coordinates.  
  
## Remarks  
 Coordinates are in pixels relative to the upper-left corner of the toolbar.  
  
 Use `GetItemRect` to get the coordinates of a separator you want to replace with a combo box or other control.  
  
## Example  
 See the example for [CToolBar::SetSizes](../vs140/CToolBar--SetSizes.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::CommandToIndex](../vs140/CToolBar--CommandToIndex.md)