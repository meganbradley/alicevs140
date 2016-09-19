---
title: "COlePropertiesDialog::m_vp"
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
ms.assetid: 26774799-7a10-47ba-b21e-889d85b14254
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertiesDialog::m_vp
A structure of type [OLEUIVIEWPROPS](http://msdn.microsoft.com/library/windows/desktop/ms693751), used to initialize the View page of the OLE Object Properties dialog box.  
  
## Syntax  
  
```  
  
OLEUIVIEWPROPS m_vp;  
  
```  
  
## Remarks  
 This page allows the user to toggle between "content" and "iconic" views of the object, and change its scaling within the container. It also allows the user access to the Change Icon dialog box when the object is being displayed as an icon.  
  
 For more information on the **OLEUIVIEWPROPS** structure, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePropertiesDialog Class](../vs140/COlePropertiesDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)