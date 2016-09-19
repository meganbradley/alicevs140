---
title: "Controls: General Support Classes"
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
ms.assetid: cf73f1d2-7542-48e3-b8c8-9d3abf29f85b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Controls: General Support Classes
The following classes provide general support for ATL controls:  
  
-   [CComControl](../vs140/CComControl-Class.md) Consists of helper functions and data members that are essential to ATL controls.  
  
-   [IOleControlImpl](../vs140/IOleControlImpl-Class.md) Provides methods necessary for controls.  
  
-   [IOleObjectImpl](../vs140/IOleObjectImpl-Class.md) Provides the principal methods through which a container communicates with a control. Manages the activation and deactivation of in-place controls.  
  
-   [IQuickActivateImpl](../vs140/IQuickActivateImpl-Class.md) Combines initialization into a single call to help containers avoid delays when loading controls.  
  
-   [IPointerInactiveImpl](../vs140/IPointerInactiveImpl-Class.md) Provides minimal mouse interaction for an otherwise inactive control.  
  
## Sample Program  
 [ATLFire](../vs140/Visual-C---Samples.md)  
  
## Related Articles  
 [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md)  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)