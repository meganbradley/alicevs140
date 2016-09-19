---
title: "ATL COM Property Pages"
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
ms.assetid: 663c7caa-2e5e-4b5c-b8ea-fd434ceb1654
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL COM Property Pages
COM property pages provide a user interface for setting the properties (or calling the methods) of one or more COM objects. Property pages are used extensively by ActiveX controls for providing rich user interfaces that allow control properties to be set at design time.  
  
 Property pages are COM objects that implement the [IPropertyPage](http://msdn.microsoft.com/library/windows/desktop/ms691246) or [IPropertyPage2](http://msdn.microsoft.com/library/windows/desktop/ms683996) interface. These interfaces provide methods that allow the page to be associated with a `site` (a COM object representing the container of the page) and a number of *objects* (COM objects whose methods will be called in response to changes made by the user of the property page). The property page container is responsible for calling methods on the property page interface to tell the page when to show or hide its user interface, and when to apply the changes made by the user to the underlying objects.  
  
 Each property page can be built completely independently of the objects whose properties can be set. All that a property page needs is to understand a particular interface (or set of interfaces) and to provide a user interface for calling methods on that interface.  
  
 For more information, see [Property Sheets and Property Pages](http://msdn.microsoft.com/library/windows/desktop/ms686577) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## In This Section  
 [Specifying Property Pages](../vs140/Specifying-Property-Pages.md)  
 Lists the steps for specifying property pages for you control and shows an example class.  
  
 [Implementing Property Pages](../vs140/Implementing-Property-Pages.md)  
 Lists the steps for implementing property pages, including methods to override. Walks you through a complete example based on the ATLPages sample program.  
  
## Related Sections  
 [ATLPages Sample](../vs140/Visual-C---Samples.md)  
 The sample abstract for the ATLPages sample, which implements a property page using `IPropertyPageImpl`.  
  
 [ATL](../vs140/Active-Template-Library--ATL--Concepts.md)  
 Provides links to conceptual topics on how to program using the Active Template Library.  
  
## See Also  
 [ATL](../vs140/Active-Template-Library--ATL--Concepts.md)