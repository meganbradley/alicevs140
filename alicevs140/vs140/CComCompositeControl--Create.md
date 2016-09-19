---
title: "CComCompositeControl::Create"
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
ms.assetid: 9f229806-1d54-4799-9090-c3f5f1cb8c3a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCompositeControl::Create
This method is called to create the control window for the composite control.  
  
## Syntax  
  
```  
  
      HWND Create(  
   HWND hWndParent,  
   RECT& /* rcPos */,  
   LPARAM dwInitParam = NULL   
);  
```  
  
#### Parameters  
 `hWndParent`  
 A handle to the parent window of the control.  
  
 `rcPos`  
 Reserved.  
  
 `dwInitParam`  
 Data to be passed to the control during control creation. The data passed as `dwInitParam` will show up as the **LPARAM** parameter of the [WM_INITDIALOG](http://msdn.microsoft.com/library/windows/desktop/ms645428) message, which will be sent to the composite control when it gets created.  
  
## Return Value  
 A handle to the newly created composite control dialog box.  
  
## Remarks  
 This method is usually called during in-place activation of the control.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCompositeControl Class](../vs140/CComCompositeControl-Class.md)   
 [AtlAxCreateDialog](../vs140/AtlAxCreateDialog.md)   
 [CComCompositeControl::CreateControlWindow](../vs140/CComCompositeControl--CreateControlWindow.md)