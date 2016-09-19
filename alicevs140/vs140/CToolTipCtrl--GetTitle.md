---
title: "CToolTipCtrl::GetTitle"
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
ms.assetid: 9b2c9c75-b6bd-4da9-9f9c-0e84b6030587
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::GetTitle
Retrieves the title of the current tooltip control.  
  
## Syntax  
  
```  
void GetTitle(  
     PTTGETTITLE pttgt  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `pttgt`|Pointer to a [TTGETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760260) structure that contains information about the ToolTip control. When this method returns, the `pszTitle` member of the [TTGETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760260) structure points to the text of the title.|  
  
## Remarks  
 This method sends the [TTM_GETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760396) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TTM_GETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760396)   
 [TTGETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760260)