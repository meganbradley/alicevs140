---
title: "CToolBarCtrl::GetButtonText"
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
ms.assetid: fd4dea0e-0e11-4618-b16e-7f9b9bf75c99
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetButtonText
Retrieves the display text of a specified button on the current toolbar control.  
  
## Syntax  
  
```  
CString GetButtonText(  
        int idButton  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `idButton`|The identifier for the button whose display text is retrieved.|  
  
## Return Value  
 A [CString](../vs140/Using-CString.md) that contains the display text of the specified button.  
  
## Remarks  
 This method sends the [TB_GETBUTTONTEXT](http://msdn.microsoft.com/library/windows/desktop/bb787325) message, which is described in the Windows SDK.  
  
## Requirements  
 This function is supported by Windows 95 and later.  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)