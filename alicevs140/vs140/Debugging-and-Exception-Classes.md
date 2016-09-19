---
title: "Debugging and Exception Classes"
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
ms.assetid: 0d158efd-2e62-452e-9d2a-d3c30dfee7f9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debugging and Exception Classes
These classes provide support for debugging dynamic memory allocation and for passing exception information from the function where the exception is thrown to the function where it is caught.  
  
 Use classes [CDumpContext](../vs140/CDumpContext-Class.md) and [CMemoryState](../vs140/CMemoryState-Structure.md) during development to assist with debugging, as described in [Debugging MFC Applications](../vs140/MFC-Debugging-Techniques.md). Use [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) to determine the class of any object at run time, as described in the article [Accessing Run-Time Class Information](../vs140/Accessing-Run-Time-Class-Information.md). The framework uses `CRuntimeClass` to create objects of a particular class dynamically.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)