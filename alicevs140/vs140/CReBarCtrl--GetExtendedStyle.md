---
title: "CReBarCtrl::GetExtendedStyle"
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
ms.assetid: 2f2284c2-946a-4c8f-a1a2-fc9cc803c65c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetExtendedStyle
Gets the extended styles of the current rebar control.  
  
## Syntax  
  
```  
DWORD GetExtendedStyle() const;  
```  
  
## Return Value  
 A bitwise combination (OR) of flags that indicate the extended styles. The possible flags are `RBS_EX_SPLITTER` and `RBS_EX_TRANSPARENT`. For more information, see the `dwMask` parameter of the [CReBarCtrl::SetExtendedStyle](../vs140/CReBarCtrl--SetExtendedStyle.md) method.  
  
## Remarks  
 This method sends the [RB_GETEXTENDEDSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb774433) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [RB_GETEXTENDEDSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb774433)   
 [CReBarCtrl::CreateEx](../vs140/CReBarCtrl--CreateEx.md)