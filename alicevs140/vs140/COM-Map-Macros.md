---
title: "COM Map Macros"
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
ms.topic: reference
ms.assetid: 0f33656d-321f-4996-90cc-9a7f21ab73c3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM Map Macros
These macros define COM interface maps.  
  
|||  
|-|-|  
|[BEGIN_COM_MAP](../vs140/BEGIN_COM_MAP.md)|Marks the beginning of the COM interface map entries.|  
|[COM_INTERFACE_ENTRY](../vs140/COM_INTERFACE_ENTRY-Macros.md)|Enters interfaces into the COM interface map.|  
|[COM_INTERFACE_ENTRY2](../vs140/COM_INTERFACE_ENTRY2.md)|Use this macro to disambiguate two branches of inheritance.|  
|[COM_INTERFACE_ENTRY_IID](../vs140/COM_INTERFACE_ENTRY_IID.md)|Use this macro to enter the interface into the COM map and specify its IID.|  
|[COM_INTERFACE_ENTRY2_IID](../vs140/COM_INTERFACE_ENTRY2_IID.md)|Same as [COM_INTERFACE_ENTRY2](../vs140/COM_INTERFACE_ENTRY2.md), except you can specify a different IID.|  
|[COM_INTERFACE_ENTRY_AGGREGATE](../vs140/COM_INTERFACE_ENTRY_AGGREGATE.md)|When the interface identified by `iid` is queried for, `COM_INTERFACE_ENTRY_AGGREGATE` forwards to `punk`.|  
|[COM_INTERFACE_ENTRY_AGGREGATE_BLIND](../vs140/COM_INTERFACE_ENTRY_AGGREGATE_BLIND.md)|Same as [COM_INTERFACE_ENTRY_AGGREGATE](../vs140/COM_INTERFACE_ENTRY_AGGREGATE.md), except that querying for any IID results in forwarding the query to `punk`.|  
|[COM_INTERFACE_ENTRY_AUTOAGGREGATE](../vs140/COM_INTERFACE_ENTRY_AUTOAGGREGATE.md)|Same as [COM_INTERFACE_ENTRY_AGGREGATE](../vs140/COM_INTERFACE_ENTRY_AGGREGATE.md), except if `punk` is **NULL**, it automatically creates the aggregate described by the `clsid`.|  
|[COM_INTERFACE_ENTRY_AUTOAGGREGATE_BLIND](../vs140/COM_INTERFACE_ENTRY_AUTOAGGREGATE_BLIND.md)|Same as [COM_INTERFACE_ENTRY_AUTOAGGREGATE](../vs140/COM_INTERFACE_ENTRY_AUTOAGGREGATE.md), except that querying for any IID results in forwarding the query to `punk`, and if `punk` is **NULL**, automatically creating the aggregate described by the `clsid`.|  
|[COM_INTERFACE_ENTRY_BREAK](../vs140/COM_INTERFACE_ENTRY_BREAK.md)|Causes your program to call [DebugBreak](http://msdn.microsoft.com/library/windows/desktop/ms679297) when the specified interface is queried for.|  
|[COM_INTERFACE_ENTRY_CACHED_TEAR_OFF](../vs140/COM_INTERFACE_ENTRY_CACHED_TEAR_OFF.md)|Saves the interface-specific data for every instance.|  
|[COM_INTERFACE_ENTRY_TEAR_OFF](../vs140/COM_INTERFACE_ENTRY_TEAR_OFF.md)|Exposes your tear-off interfaces.|  
|[COM_INTERFACE_ENTRY_CHAIN](../vs140/COM_INTERFACE_ENTRY_CHAIN.md)|Processes the COM map of the base class when the processing reaches this entry in the COM map.|  
|[COM_INTERFACE_ENTRY_FUNC](../vs140/COM_INTERFACE_ENTRY_FUNC.md)|A general mechanism for hooking into ATL's `QueryInterface` logic.|  
|[COM_INTERFACE_ENTRY_FUNC_BLIND](../vs140/COM_INTERFACE_ENTRY_FUNC_BLIND.md)|Same as [COM_INTERFACE_ENTRY_FUNC](../vs140/COM_INTERFACE_ENTRY_FUNC.md), except that querying for any IID results in a call to `func`.|  
|[COM_INTERFACE_ENTRY_NOINTERFACE](../vs140/COM_INTERFACE_ENTRY_NOINTERFACE.md)|Returns **E_NOINTERFACE** and terminates COM map processing when the specified interface is queried for.|  
|[END_COM_MAP](../vs140/END_COM_MAP.md)|Marks the end of the COM interface map entries.|  
  
## See Also  
 [Macros](../vs140/ATL-Macros.md)   
 [COM Map Global Functions](../vs140/COM-Map-Global-Functions.md)