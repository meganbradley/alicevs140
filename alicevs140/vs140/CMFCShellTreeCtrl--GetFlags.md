---
title: "CMFCShellTreeCtrl::GetFlags"
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
ms.assetid: bb3208fc-1b0f-4391-af4b-1328ff6747fd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellTreeCtrl::GetFlags
Returns the flags set for the [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md) object.  
  
## Syntax  
  
```  
DWORD GetFlags() const;  
```  
  
## Return Value  
 A `DWORD` value that specifies the combination of flags currently set.  
  
## Remarks  
 The flags set in the `CMFCShellTreeCtrl` are sent to the method [IShellFolder::EnumObjects](http://msdn.microsoft.com/library/windows/desktop/bb775066) whenever the object is refreshed. You can change the flags with the [CMFCShellTreeCtrl::SetFlags](../vs140/CMFCShellTreeCtrl--SetFlags.md) method.  
  
## Requirements  
 **Header:** afxshelltreectrl.h  
  
## See Also  
 [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCShellTreeCtrl::SetFlags](../vs140/CMFCShellTreeCtrl--SetFlags.md)