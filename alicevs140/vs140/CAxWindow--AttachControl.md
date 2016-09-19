---
title: "CAxWindow::AttachControl"
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
ms.assetid: ed80db40-eb52-4746-b46c-f8aff681c318
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxWindow::AttachControl
Creates a new host object if one isn't already present and attaches the specified control to the host.  
  
## Syntax  
  
```  
  
      HRESULT AttachControl(  
   IUnknown* pControl,  
   IUnknown** ppUnkContainer   
);  
```  
  
#### Parameters  
 `pControl`  
 [in] A pointer to the **IUnknown** of the control.  
  
 `ppUnkContainer`  
 [out] A pointer to the **IUnknown** of the host (the **AxWin** object).  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The control object being attached must be correctly initialized before calling `AttachControl`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxWindow Class](../vs140/CAxWindow-Class.md)   
 [AtlAxAttachControl](../vs140/AtlAxAttachControl.md)