---
title: "CButton::GetSplitStyle"
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
ms.assetid: 06ecdb56-aa77-454f-83e0-eaabc953d2ae
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetSplitStyle
Retrieves the split button styles that define the current split button control.  
  
## Syntax  
  
```  
UINT GetSplitStyle() const;  
```  
  
## Return Value  
 A bitwise combination of split button styles. For more information, see the `uSplitStyle` member of the [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955) structure.  
  
## Remarks  
 Use this method only with controls whose button style is `BS_SPLITBUTTON` or `BS_DEFSPLITBUTTON`.  
  
 The split button styles specify the alignment, aspect ratio, and graphical format with which Windows draws a split button icon.  
  
 This method initializes the `mask` member of a [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955) structure with the `BCSIF_STYLE` flag, and then sends that structure in the [BCM_GETSPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775969) message that is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. When the message function returns, this method retrieves the split button styles from the `uSplitStyle` member of the structure.  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetSplitStyle](../vs140/CButton--SetSplitStyle.md)   
 [CButton::GetSplitInfo](../vs140/CButton--GetSplitInfo.md)   
 [BCM_GETSPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775969)