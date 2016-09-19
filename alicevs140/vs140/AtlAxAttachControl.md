---
title: "AtlAxAttachControl"
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
ms.assetid: 80b5b2e8-dc67-4b22-ba95-632a089dbe47
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlAxAttachControl
Attaches a previously created control to the specified window.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLAPI AtlAxAttachControl(  
IUnknown* pControl,  
HWND hWnd,  
IUnknown** ppUnkContainer   
);  
```  
  
#### Parameters  
 `pControl`  
 [in] A pointer to the **IUnknown** of the control.  
  
 `hWnd`  
 [in] Handle to the window that will host the control.  
  
 `ppUnkContainer`  
 [out] A pointer to a pointer to the **IUnknown** of the container object.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 Use [AtlAxCreateControlEx](../vs140/AtlAxCreateControlEx.md) and [AtlAxCreateControl](../vs140/AtlAxCreateControl.md) to simultaneously create and attach a control.  
  
> [!NOTE]
>  The control object being attached must be correctly initialized before calling `AtlAxAttachControl`.  
  
## Requirements  
 **Header:** atlhost.h  
  
## See Also  
 [Composite Control Fundamentals](../vs140/ATL-Composite-Control-Fundamentals.md)