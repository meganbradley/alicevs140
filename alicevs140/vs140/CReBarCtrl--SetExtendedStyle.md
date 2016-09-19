---
title: "CReBarCtrl::SetExtendedStyle"
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
ms.assetid: 64d74966-2556-48ac-b2a3-408559f8d413
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetExtendedStyle
Sets the extended styles for the current rebar control.  
  
## Syntax  
  
```  
DWORD SetExtendedStyle(  
      DWORD dwMask,   
      DWORD dwStyleEx  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwMask`|A bitwise combination (OR) of flags that specify which flags in the `dwStyleEx` parameter apply. Use one or more of the following values:<br /><br /> RBS_EX_SPLITTER: By default, show the splitter on the bottom in horizontal mode, and to the right in vertical mode.<br /><br /> RBS_EX_TRANSPARENT: Forward the [WM_ERASEBKGND](http://msdn.microsoft.com/library/windows/desktop/ms648055) message to the parent window.|  
|[in] `dwStyleEx`|A bitwise combination (OR) of flags that specify the styles to apply. To set a style, specify the same flag that is used in the `dwMask` parameter. To reset a style, specify binary zero.|  
  
## Return Value  
 The previous extended style.  
  
## Remarks  
 This method sends the [RB_SETEXTENDEDSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb774519) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)