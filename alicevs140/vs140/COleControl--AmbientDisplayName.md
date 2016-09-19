---
title: "COleControl::AmbientDisplayName"
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
ms.assetid: cc06acc4-c5a1-4e4b-96da-9cd783999cbc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientDisplayName
The name the container has assigned to the control can be used in error messages displayed to the user.  
  
## Syntax  
  
```  
  
CString AmbientDisplayName( );  
```  
  
## Return Value  
 The name of the OLE control. The default is a zero-length string.  
  
## Remarks  
 Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)