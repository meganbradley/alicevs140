---
title: "CComboBox::GetComboBoxInfo"
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
ms.assetid: dad7cbe4-8417-419c-8fc8-0af33e502b4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetComboBoxInfo
Retrieves information for the `CComboBox` object.  
  
## Syntax  
  
```  
  
      BOOL GetComboBoxInfo(  
   PCOMBOBOXINFO pcbi  
) const;  
```  
  
#### Parameters  
 *pcbi*  
 A pointer to the [COMBOBOXINFO](http://msdn.microsoft.com/library/windows/desktop/bb775798) structure.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function emulates the functionality of the [CB_GETCOMBOBOXINFO](http://msdn.microsoft.com/library/windows/desktop/bb775839) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)