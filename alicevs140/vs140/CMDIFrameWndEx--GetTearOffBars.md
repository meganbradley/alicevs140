---
title: "CMDIFrameWndEx::GetTearOffBars"
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
ms.assetid: fbbbdecd-16aa-4203-a7e8-c88d0673b709
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::GetTearOffBars
Returns a list of tear-off menus.  
  
## Syntax  
  
```  
const CObList& GetTearOffBars() const;  
```  
  
## Return Value  
 A reference to a [CObList Class](../vs140/CObList-Class.md) object that contains a collection of pointers to `CPane`-derived objects that are in a tear-off state.  
  
## Remarks  
 `CMDIFrameWndEx` maintains a collection of tear-off menus. Use this method to retrieve a reference to this list.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)