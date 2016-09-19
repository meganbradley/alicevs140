---
title: "Interfaces (ATL)"
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
ms.assetid: de6c8b12-6230-4fdc-af66-a28b91d5ee55
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Interfaces (ATL)
An interface is the way in which an object exposes its functionality to the outside world. In COM, an interface is a table of pointers (like a C++ vtable) to functions implemented by the object. The table represents the interface, and the functions to which it points are the methods of that interface. An object can expose as many interfaces as it chooses.  
  
 Each interface is based on the fundamental COM interface, [IUnknown](../vs140/IUnknown.md). The methods of **IUnknown** allow navigation to other interfaces exposed by the object.  
  
 Also, each interface is given a unique interface ID (IID). This uniqueness makes it easy to support interface versioning. A new version of an interface is simply a new interface, with a new IID.  
  
> [!NOTE]
>  IIDs for the standard COM and OLE interfaces are predefined.  
  
## See Also  
 [Introduction to COM](../vs140/Introduction-to-COM.md)   
 [COM Objects and Interfaces](http://msdn.microsoft.com/library/windows/desktop/ms690343)