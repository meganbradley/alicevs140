---
title: "Registering OLE Controls"
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
ms.assetid: 73c45b7f-7dbc-43f5-bd17-dd77c6acec72
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Registering OLE Controls
OLE controls, like other OLE server objects, can be accessed by other OLE-aware applications. This is achieved by registering the control's type library and class.  
  
 The following functions allow you to add and remove the control's class, property pages, and type library in the Windows registration database:  
  
### Registering OLE Controls  
  
|||  
|-|-|  
|[AfxOleRegisterControlClass](../vs140/AfxOleRegisterControlClass.md)|Adds the control's class to the registration database.|  
|[AfxOleRegisterPropertyPageClass](../vs140/AfxOleRegisterPropertyPageClass.md)|Adds a control property page to the registration database.|  
|[AfxOleRegisterTypeLib](../vs140/AfxOleRegisterTypeLib.md)|Adds the control's type library to the registration database.|  
|[AfxOleUnregisterClass](../vs140/AfxOleUnregisterClass.md)|Removes a control class or a property page class from the registration database.|  
|[AfxOleUnregisterTypeLib](../vs140/AfxOleUnregisterTypeLib.md)|Removes the control's type library from the registration database.|  
  
 `AfxOleRegisterTypeLib` is typically called in a control DLL's implementation of `DllRegisterServer`. Similarly, `AfxOleUnregisterTypeLib` is called by `DllUnregisterServer`. `AfxOleRegisterControlClass`, `AfxOleRegisterPropertyPageClass`, and `AfxOleUnregisterClass` are typically called by the `UpdateRegistry` member function of a control's class factory or property page.  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)