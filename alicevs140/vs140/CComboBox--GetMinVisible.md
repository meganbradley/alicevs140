---
title: "CComboBox::GetMinVisible"
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
ms.assetid: d24382fe-947e-4468-b8db-4139230049c0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetMinVisible
Gets the minimum number of visible items in the drop-down list of the current combo box control.  
  
## Syntax  
  
```  
int GetMinVisible() const;  
```  
  
## Return Value  
 The minimum number of visible items in the current drop-down list.  
  
## Remarks  
 This method sends the [CB_GETMINVISIBLE](http://msdn.microsoft.com/library/windows/desktop/bb775915) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetMinVisibleItems](../vs140/CComboBox--SetMinVisibleItems.md)   
 [CComboBox::ShowDropDown](../vs140/CComboBox--ShowDropDown.md)   
 [CB_GETMINVISIBLE](http://msdn.microsoft.com/library/windows/desktop/bb775915)