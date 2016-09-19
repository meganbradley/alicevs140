---
title: "CToolBarCtrl::MapAccelerator"
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
ms.assetid: 93584e00-5012-4ec1-a633-c5bba615751d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::MapAccelerator
Maps an accelerator character to a toolbar button.  
  
## Syntax  
  
```  
  
      BOOL MapAccelerator(  
   TCHAR chAccel,  
   UINT* pIDBtn   
);  
```  
  
#### Parameters  
 `chAccel`  
 Accelerator character to be mapped. This character is the same character that is underlined in the button's text.  
  
 *pIDBtn*  
 A pointer to a **UINT** that receives the command identifier of the button that corresponds to the accelerator specified in `chAccel`.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_MAPACCELERATOR](http://msdn.microsoft.com/library/windows/desktop/bb787383), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)