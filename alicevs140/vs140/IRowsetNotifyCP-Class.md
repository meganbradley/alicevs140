---
title: "IRowsetNotifyCP Class"
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
ms.assetid: ccef402b-94a0-4c2e-9a13-7e854ef82390
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetNotifyCP Class
Implements the provider site for the connection point interface [IRowsetNotify](https://msdn.microsoft.com/en-us/library/ms712959.aspx).  
  
## Syntax  
  
```  
template <  
   class T,   
   class ReentrantEventSync = CComSharedMutex   
>  
class IRowsetNotifyCP :   
   public IConnectionPointImpl<  
      T,   
      piid = &__uuidof(IRowsetNotify),   
      CComDynamicUnkArray DynamicUnkArray  
   >,  
   public ReentrantEventSync  
```  
  
#### Parameters  
 `T`  
 A class derived from `IRowsetNotifyCP`.  
  
 `ReentrantEventSync`  
 A mutex class that supports reentrancy (the default is **CComSharedMutex**). A mutex is a synchronization object that allows one thread mutually exclusive access to a resource.  
  
 `piid`  
 A interface ID pointer (**IID\***) for an **IRowsetNotify** connection point interface. The default value is **&__uuidof(IRowsetNotify)**.  
  
 `DynamicUnkArray`  
 An array of type [CComDynamicUnkArray](../vs140/CComDynamicUnkArray-Class.md), which is a dynamically allocated array of **IUnknown** pointers to the client sink interfaces.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[Fire_OnFieldChange](../vs140/IRowsetNotifyCP--Fire_OnFieldChange.md)|Notifies the consumer of a change to the value of a column.|  
|[Fire_OnRowChange](../vs140/IRowsetNotifyCP--Fire_OnRowChange.md)|Notifies the consumer of a change affecting the rows.|  
|[Fire_OnRowsetChange](../vs140/IRowsetNotifyCP--Fire_OnRowsetChange.md)|Notifies the consumer of a change affecting the entire rowset.|  
  
## Remarks  
 `IRowsetNotifyCP` implements broadcast functions to advise listeners on the connection point **IID_IRowsetNotify** of changes to the contents of the rowset.  
  
 Note that you must also implement and register `IRowsetNotify` on the consumer (also known as the "sink") using [IRowsetNotifyImpl](../vs140/IRowsetNotifyImpl-Class.md) so that the consumer can handle notifications. See [Receiving Notifications](../vs140/Receiving-Notifications.md) about implementing the connection point interface on the consumer.  
  
 For detailed information on implementing notifications, see "Supporting Notifications" in [Creating an Updatable Provider](../vs140/Creating-an-Updatable-Provider.md).  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)   
 [Notifications (COM)](http://msdn.microsoft.com/library/windows/desktop/ms678433)   
 [Overview of Notifications (OLE DB)](https://msdn.microsoft.com/en-us/library/ms725406.aspx)   
 [BEGIN_CONNECTION_POINT_MAP](../vs140/BEGIN_CONNECTION_POINT_MAP.md)   
 [END_CONNECTION_POINT_MAP](../vs140/END_CONNECTION_POINT_MAP.md)   
 [CONNECTION_POINT_ENTRY](../vs140/CONNECTION_POINT_ENTRY.md)   
 [Creating an Updatable Provider](../vs140/Creating-an-Updatable-Provider.md)