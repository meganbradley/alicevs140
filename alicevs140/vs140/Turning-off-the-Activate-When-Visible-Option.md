---
title: "Turning off the Activate When Visible Option"
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
ms.topic: article
ms.assetid: 8f7ddc5a-a7a6-4da8-bcb9-1b569f0ecb48
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Turning off the Activate When Visible Option
A control has two basic states: active and inactive. Traditionally, these states were distinguished by whether the control had a window. An active control had a window; an inactive control did not. With the introduction of windowless activation, this distinction is no longer universal, but still applies to many controls.  
  
 Compared with the rest of the initialization typically performed by an ActiveX control, the creation of a window is an extremely expensive operation. Ideally, a control would defer creating its window until absolutely necessary.  
  
 Many controls do not need to be active the entire time they are visible in a container. Often, a control can remain in the inactive state until the user performs an operation that requires it to become active (for example, clicking with the mouse or pressing the TAB key). To cause a control to remain inactive until the container needs to activate it, remove the **OLEMISC_ACTIVATEWHENVISIBLE** flag from the control's miscellaneous flags:  
  
 [!CODE [NVC_MFC_AxOpt#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxOpt#9)]  
  
 The **OLEMISC_ACTIVATEWHENVISIBLE** flag is automatically omitted if you turn off the **Activate When Visible** option in the [Control Settings](../vs140/Control-Settings--MFC-ActiveX-Control-Wizard.md) page of the MFC ActiveX Control Wizard when you create your control.  
  
## See Also  
 [MFC ActiveX Controls: Optimization](../vs140/MFC-ActiveX-Controls--Optimization.md)