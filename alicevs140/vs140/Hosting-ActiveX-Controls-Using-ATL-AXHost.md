---
title: "Hosting ActiveX Controls Using ATL AXHost"
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
ms.assetid: 2c1200ec-effb-4814-820a-509519699468
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Hosting ActiveX Controls Using ATL AXHost
The sample in this topic shows how to create AXHost and how to host an ActiveX control using various ATL functions. It also shows how to access the control and sink events (using [IDispEventImpl](../vs140/IDispEventImpl-Class.md)) from the control that is hosted. The sample hosts the Calendar control in a main window or in a child window.  
  
 Notice the definition of the `USE_METHOD` symbol. You can change the value of this symbol to vary between 1 and 8. The value of the symbol determines how the control will be created:  
  
-   For even-numbered values of `USE_METHOD`, the call to create the host subclasses a window and converts it into a control host. For odd-numbered values, the code creates a child window that acts as a host.  
  
-   For values of `USE_METHOD` between 1 and 4, access to the control and sinking of events are accomplished in the call that also creates the host. Values between 5 and 8 query the host for interfaces and hook the sink.  
  
 Here's a summary:  
  
|USE_METHOD|Host|Control access and event sinking|Function demonstrated|  
|-----------------|----------|--------------------------------------|---------------------------|  
|1|Child window|One step|CreateControlLicEx|  
|2|Main window|One step|AtlAxCreateControlLicEx|  
|3|Child window|One step|CreateControlEx|  
|4|Main window|One step|AtlAxCreateControlEx|  
|5|Child window|Multiple steps|CreateControlLic|  
|6|Main window|Multiple steps|AtlAxCreateControlLic|  
|7|Child window|Multiple steps|CreateControl|  
|8|Main window|Multiple steps|AtlAxCreateControl|  
  
 [!CODE [NVC_ATL_AxHost#1](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_AxHost#1)]  
  
## See Also  
 [Control Containment FAQ](../vs140/ATL-Control-Containment-FAQ.md)   
 [AtlAxCreateControl](../vs140/AtlAxCreateControl.md)   
 [AtlAxCreateControlEx](../vs140/AtlAxCreateControlEx.md)   
 [AtlAxCreateControlLic](../vs140/AtlAxCreateControlLic.md)   
 [AtlAxCreateControlLicEx](../vs140/AtlAxCreateControlLicEx.md)   
 [CAxWindow2T Class](../vs140/CAxWindow2T-Class.md)   
 [IAxWinHostWindowLic Interface](../vs140/IAxWinHostWindowLic-Interface.md)