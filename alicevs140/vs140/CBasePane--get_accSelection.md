---
title: "CBasePane::get_accSelection"
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
ms.assetid: 902b0b7d-5314-433d-b7b5-7822f1730ab1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::get_accSelection
The framework calls this method to retrieve the selected children of this object.  
  
## Syntax  
  
```  
virtual HRESULT get_accSelection(  
   VARIANT *pvarChildren  
);  
```  
  
#### Parameters  
 [in] `pvarChildren`  
 Receives information that identifies the selected children.  
  
## Return Value  
 `CBasePane` does not implement this method. If `pvarChildren` is `NULL`, this method returns `E_INVALIDARG`. Otherwise, this method returns `DISP_E_MEMBERNOTFOUND`.  
  
## Remarks  
 This function is part of the Active Accessibility support in MFC. Override this function in a derived class if you have non-windowed user interface elements other than windowless ActiveX controls.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)