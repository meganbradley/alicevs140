---
title: "UI Support Classes"
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
ms.assetid: 313dfc95-308a-4118-b919-5a3c3673b865
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UI Support Classes
The following classes provide general UI support:  
  
-   [IDocHostUIHandlerDispatch](../vs140/IDocHostUIHandlerDispatch-Interface.md) An interface to the Microsoft HTML parsing and rendering engine.  
  
-   [IOleObjectImpl](../vs140/IOleObjectImpl-Class.md) Provides the principal methods through which a container communicates with a control. Manages the activation and deactivation of in-place controls.  
  
-   [IOleInPlaceObjectWindowlessImpl](../vs140/IOleInPlaceObjectWindowlessImpl-Class.md) Manages the reactivation of in-place controls. Enables a windowless control to receive messages, as well as to participate in drag-and-drop operations.  
  
-   [IOleInPlaceActiveObjectImpl](../vs140/IOleInPlaceActiveObjectImpl-Class.md) Assists communication between an in-place control and its container.  
  
-   [IViewObjectExImpl](../vs140/IViewObjectExImpl-Class.md) Enables a control to display itself directly and to notify the container of changes in its display. Provides support for flicker-free drawing, non-rectangular and transparent controls, and hit testing.  
  
## Related Articles  
 [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md)  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)