---
title: "CMenu::FromHandle"
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
ms.assetid: 6bd1e029-2e89-450c-8483-89a15b487892
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::FromHandle
Returns a pointer to a `CMenu` object given a Windows handle to a menu.  
  
## Syntax  
  
```  
  
      static CMenu* PASCAL FromHandle(  
   HMENU hMenu   
);  
```  
  
#### Parameters  
 `hMenu`  
 A Windows handle to a menu.  
  
## Return Value  
 A pointer to a `CMenu` that may be temporary or permanent.  
  
## Remarks  
 If a `CMenu` object is not already attached to the Windows menu object, a temporary `CMenu` object is created and attached.  
  
 This temporary `CMenu` object is only valid until the next time the application has idle time in its event loop, at which time all temporary objects are deleted.  
  
## Example  
 See the example for [CMenu::CreateMenu](../vs140/CMenu--CreateMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)