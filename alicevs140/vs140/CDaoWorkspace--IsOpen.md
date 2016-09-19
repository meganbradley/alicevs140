---
title: "CDaoWorkspace::IsOpen"
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
ms.assetid: 7b6f9f54-7d4f-4bb4-ad45-89b067094092
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::IsOpen
Call this member function to determine whether the `CDaoWorkspace` object is open — that is, whether the MFC object has been initialized by a call to [Open](../vs140/CDaoWorkspace--Open.md) or a call to [Create](../vs140/CDaoWorkspace--Create.md).  
  
## Syntax  
  
```  
  
BOOL IsOpen( ) const;  
  
```  
  
## Return Value  
 Nonzero if the workspace object is open; otherwise 0.  
  
## Remarks  
 You can call any of the member functions of a workspace that is in an open state.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)