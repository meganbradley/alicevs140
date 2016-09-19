---
title: "Introduction to COM"
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
ms.topic: index-page 
ms.assetid: 120735d9-db71-4ad3-a730-ce576ea2354e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Introduction to COM
COM is the fundamental "object model" on which ActiveX Controls and OLE are built. COM allows an object to expose its functionality to other components and to host applications. It defines both how the object exposes itself and how this exposure works across processes and across networks. COM also defines the object's life cycle.  
  
 Fundamental to COM are these concepts:  
  
-   [Interfaces](../vs140/Interfaces--ATL-.md) — the mechanism through which an object exposes its functionality.  
  
-   [IUnknown](../vs140/IUnknown.md) — the basic interface on which all others are based. It implements the reference counting and interface querying mechanisms running through COM.  
  
-   [Reference counting](../vs140/Reference-Counting.md) — the technique by which an object (or, strictly, an interface) decides when it is no longer being used and is therefore free to remove itself.  
  
-   [QueryInterface](../vs140/QueryInterface.md) — the method used to query an object for a given interface.  
  
-   [Marshaling](../vs140/Marshaling.md) — the mechanism that enables objects to be used across thread, process, and network boundaries, allowing for location independence.  
  
-   [Aggregation](../vs140/Aggregation.md) — a way in which one object can make use of another.  
  
## See Also  
 [Introduction to COM and ATL](../vs140/Introduction-to-COM-and-ATL.md)   
 [The Component Object Model](http://msdn.microsoft.com/library/windows/desktop/ms694363)