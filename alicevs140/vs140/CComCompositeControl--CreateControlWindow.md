---
title: "CComCompositeControl::CreateControlWindow"
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
ms.assetid: 0cf7f4c8-f1c4-487b-b293-9de12a61af2e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCompositeControl::CreateControlWindow
Call this method to create the control window and advise any hosted controls.  
  
## Syntax  
  
```  
  
      virtual HWND CreateControlWindow(  
   HWND hWndParent,  
   RECT& rcPos   
);  
```  
  
#### Parameters  
 `hWndParent`  
 A handle to the parent window of the control.  
  
 `rcPos`  
 The position rectangle of the composite control in client coordinates relative to `hWndParent`.  
  
## Return Value  
 Returns a handle to the newly created composite control dialog box.  
  
## Remarks  
 This method calls [CComCompositeControl::Create](../vs140/CComCompositeControl--Create.md) and [CComCompositeControl::AdviseSinkMap](../vs140/CComCompositeControl--AdviseSinkMap.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCompositeControl Class](../vs140/CComCompositeControl-Class.md)