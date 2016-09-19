---
title: "CMDIFrameWndEx::AreMDITabs"
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
ms.assetid: cffa3b14-e766-41a9-83d5-dd383a09938f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::AreMDITabs
Determines whether the MDI tabs feature or the MDI tabbed groups feature is enabled.  
  
## Syntax  
  
```  
BOOL AreMDITabs(  
   int* pnMDITabsType=NULL   
) const;  
```  
  
#### Parameters  
 [out] `pnMDITabsType`  
 A pointer to an integer variable that indicates which features are enabled:  
  
-   0: All features are disabled.  
  
-   1: MDI tabs is enabled.  
  
-   2: MDI tabbed groups is enabled.  
  
## Return Value  
 `Returns TRUE` if MDI tabs or MDI tabbed groups is enabled.  
  
 `Returns FALSE` if none of the above features is enabled.  
  
## Remarks  
 Use this function to determine whether MDI tabs or MDI tabbed groups is enabled for the frame window. Use [CMDIFrameWndEx::EnableMDITabs](../vs140/CMDIFrameWndEx--EnableMDITabs.md) to enable or disable the MDI tabs feature.  
  
 Use [CMDIFrameWndEx::EnableMDITabbedGroups](../vs140/CMDIFrameWndEx--EnableMDITabbedGroups.md) to enable or disable the MDI tabbed groups feature.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)