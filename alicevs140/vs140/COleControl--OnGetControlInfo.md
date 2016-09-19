---
title: "COleControl::OnGetControlInfo"
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
ms.assetid: c8f337c6-d698-4d6b-8307-2e69f0561f5e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnGetControlInfo
Called by the framework when the control's container has requested information about the control.  
  
## Syntax  
  
```  
  
      virtual void OnGetControlInfo(  
   LPCONTROLINFO pControlInfo   
);  
```  
  
#### Parameters  
 `pControlInfo`  
 Pointer to a [CONTROLINFO](http://msdn.microsoft.com/library/windows/desktop/ms680734) structure to be filled in.  
  
## Remarks  
 This information consists primarily of a description of the control's mnemonic keys. The default implementation fills `pControlInfo` with default information.  
  
 Override this function if your control needs to process mnemonic keys.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)