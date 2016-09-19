---
title: "COleControl::GetMessageString"
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
ms.assetid: 84dba6b7-fef9-488b-9f2c-95a24917352a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetMessageString
Called by the framework to obtain a short string that describes the purpose of the menu item identified by `nID`.  
  
## Syntax  
  
```  
  
      virtual void GetMessageString(  
   UINT nID,  
   CString& rMessage   
) const;  
```  
  
#### Parameters  
 `nID`  
 A menu item ID.  
  
 `rMessage`  
 A reference to a [CString](../vs140/CStringT-Class.md) object through which a string will be returned.  
  
## Remarks  
 This can be used to obtain a message for display in a status bar while the menu item is highlighted. The default implementation attempts to load a string resource identified by `nID`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)