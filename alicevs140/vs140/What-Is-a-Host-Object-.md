---
title: "What Is a Host Object?"
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
ms.assetid: 4f8da992-b27e-45e8-b5e0-c8b1dcae4fac
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# What Is a Host Object?
A host object is a COM object that represents the ActiveX control container supplied by ATL for a particular window. The host object subclasses the container window so that it can reflect messages to the control, it provides the necessary container interfaces to be used by the control, and it exposes the [IAxWinHostWindow](../vs140/IAxWinHostWindow-Interface.md) and [IAxWinAmbientDispatch](../vs140/IAxWinAmbientDispatch-Interface.md) interfaces to allow you to configure the environment of the control.  
  
 You can use the host object to set the ambient properties of the container.  
  
## See Also  
 [Control Containment FAQ](../vs140/ATL-Control-Containment-FAQ.md)