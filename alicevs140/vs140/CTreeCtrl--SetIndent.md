---
title: "CTreeCtrl::SetIndent"
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
ms.assetid: 4fec839d-0655-4650-b35c-10296fa0bf30
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetIndent
Call this function to set the width of indentation for a tree view control and redraw the control to reflect the new width.  
  
## Syntax  
  
```  
  
      void SetIndent(  
   UINT nIndent   
);  
```  
  
#### Parameters  
 `nIndent`  
 Width, in pixels, of the indentation. If `nIndent` is less than the system-defined minimum width, the new width is set to the system-defined minimum.  
  
## Example  
 See the example for [CTreeCtrl::GetIndent](../vs140/CTreeCtrl--GetIndent.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetIndent](../vs140/CTreeCtrl--GetIndent.md)   
 [CTreeCtrl::GetItemRect](../vs140/CTreeCtrl--GetItemRect.md)