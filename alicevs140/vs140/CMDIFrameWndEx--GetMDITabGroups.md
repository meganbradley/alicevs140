---
title: "CMDIFrameWndEx::GetMDITabGroups"
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
ms.assetid: 6ace4a34-fc05-4337-8e9b-a4389806d171
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::GetMDITabGroups
Returns a list of MDI tabbed windows.  
  
## Syntax  
  
```  
const CObList& GetMDITabGroups() const;  
```  
  
## Return Value  
 A reference to a [CObList Class](../vs140/CObList-Class.md) object that contains a list of tabbed windows. Do not store or modify the list.  
  
## Remarks  
 Use this method to access the list of tabbed windows. It can be helpful if you want to change or query some parameters of individual tabbed windows.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)