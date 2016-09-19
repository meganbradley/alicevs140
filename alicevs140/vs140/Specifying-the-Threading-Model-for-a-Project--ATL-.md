---
title: "Specifying the Threading Model for a Project (ATL)"
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
ms.assetid: 6b571078-521c-4f3e-9f08-482aa235a822
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifying the Threading Model for a Project (ATL)
The following macros are available to specify the threading model of an ATL project:  
  
|Macro|Guidelines for using|  
|-----------|--------------------------|  
|_ATL_SINGLE_THREADED|Define if all of your objects use the single threading model.|  
|_ATL_APARTMENT_THREADED|Define if one or more of your objects use apartment threading.|  
|_ATL_FREE_THREADED|Define if one or more of your objects use free or neutral threading. Existing code may contain references to the equivalent macro [_ATL_MULTI_THREADED](../vs140/_ATL_MULTI_THREADED.md).|  
  
 If you do not define any of these macros for your project, _ATL_FREE_THREADED will be in effect.  
  
 The macros affect run-time performance as follows:  
  
-   Specifying the macro that corresponds to the objects in your project can improve run-time performance.  
  
-   Specifying a higher level of macro, for example if you specify _ATL_APARTMENT_THREADED when all of your objects are single threaded, will slightly degrade run-time performance.  
  
-   Specifying a lower level of macro, for example, if you specify _ATL_SINGLE_THREADED when one or more of your objects use apartment threading or free threading, can cause your application to fail at run time.  
  
 See [Options, ATL Simple Object Wizard](../vs140/Options--ATL-Simple-Object-Wizard.md) for a description of the threading models available for an ATL object.  
  
## See Also  
 [Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)