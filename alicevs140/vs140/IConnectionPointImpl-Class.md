---
title: "IConnectionPointImpl Class"
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
ms.assetid: 27992115-3b86-45dd-bc9e-54f32876c557
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IConnectionPointImpl Class
This class implements a connection point.  
  
## Syntax  
  
```  
  
template<  
      class  T,  
      const IID*  piid,  
      class  CDV   
   = CComDynamicUnkArray >  
   class ATL_NO_VTABLE IConnectionPointImpl :  
      public _ICPLocator<  piid  
    >  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IConnectionPointImpl`.  
  
 `piid`  
 A pointer to the IID of the interface represented by the connection point object.  
  
 `CDV`  
 A class that manages the connections. The default value is [CComDynamicUnkArray](../vs140/CComDynamicUnkArray-Class.md), which allows unlimited connections. You can also use [CComUnkArray](../vs140/CComUnkArray-Class.md), which specifies a fixed number of connections.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IConnectionPointImpl::Advise](../vs140/IConnectionPointImpl--Advise.md)|Establishes a connection between the connection point and a sink.|  
|[IConnectionPointImpl::EnumConnections](../vs140/IConnectionPointImpl--EnumConnections.md)|Creates an enumerator to iterate through the connections for the connection point.|  
|[IConnectionPointImpl::GetConnectionInterface](../vs140/IConnectionPointImpl--GetConnectionInterface.md)|Retrieves the IID of the interface represented by the connection point.|  
|[IConnectionPointImpl::GetConnectionPointContainer](../vs140/IConnectionPointImpl--GetConnectionPointContainer.md)|Retrieves an interface pointer to the connectable object.|  
|[IConnectionPointImpl::Unadvise](../vs140/IConnectionPointImpl--Unadvise.md)|Terminates a connection previously established through `Advise`.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[IConnectionPointImpl::m_vec](../vs140/IConnectionPointImpl--m_vec.md)|Manages the connections for the connection point.|  
  
## Remarks  
 `IConnectionPointImpl` implements a connection point, which allows an object to expose an outgoing interface to the client. The client implements this interface on an object called a sink.  
  
 ATL uses [IConnectionPointContainerImpl](../vs140/IConnectionPointContainerImpl-Class.md) to implement the connectable object. Each connection point within the connectable object represents an outgoing interface, identified by `piid`. Class  *CDV* manages the connections between the connection point and a sink. Each connection is uniquely identified by a "cookie."  
  
 For more information about using connection points in ATL, see the article [Connection Points](../vs140/ATL-Connection-Points.md).  
  
## Inheritance Hierarchy  
 `_ICPLocator`  
  
 `IConnectionPointImpl`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="iconnectionpointimpl__advise"></a>  IConnectionPointImpl::Advise  
 Establishes a connection between the connection point and a sink.  
  
```  
  
STDMETHOD(Advise)(  
      IUnknown*  pUnkSink,  
      DWORD*  pdwCookie  
   );  
  
```  
  
### Remarks  
 Use [Unadvise](../vs140/IConnectionPointImpl--Unadvise.md) to terminate the connection call.  
  
 See [IConnectionPoint::Advise](http://msdn.microsoft.com/library/windows/desktop/ms678815) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iconnectionpointimpl__enumconnections"></a>  IConnectionPointImpl::EnumConnections  
 Creates an enumerator to iterate through the connections for the connection point.  
  
```  
  
STDMETHOD(EnumConnections)(  
      IEnumConnections**  ppEnum  
   );  
  
```  
  
### Remarks  
 See [IConnectionPoint::EnumConnections](http://msdn.microsoft.com/library/windows/desktop/ms680755) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iconnectionpointimpl__getconnectioninterface"></a>  IConnectionPointImpl::GetConnectionInterface  
 Retrieves the IID of the interface represented by the connection point.  
  
```  
  
STDMETHOD(GetConnectionInterface)(  
      IID*  piid2  
   );  
  
```  
  
### Remarks  
 See [IConnectionPoint::GetConnectionInterface](http://msdn.microsoft.com/library/windows/desktop/ms693468) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iconnectionpointimpl__getconnectionpointcontainer"></a>  IConnectionPointImpl::GetConnectionPointContainer  
 Retrieves an interface pointer to the connectable object.  
  
```  
  
STDMETHOD(GetConnectionPointContainer)(  
      IConnectionPointContainer**  ppCPC  
   );  
  
```  
  
### Remarks  
 See [IConnectionPoint::GetConnectionPointContainer](http://msdn.microsoft.com/library/windows/desktop/ms679669) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iconnectionpointimpl__m_vec"></a>  IConnectionPointImpl::m_vec  
 Manages the connections between the connection point object and a sink.  
  
```  
CDV  
  m_vec;  
  
```  
  
### Remarks  
 By default, `m_vec` is of type [CComDynamicUnkArray](../vs140/CComDynamicUnkArray-Class.md).  
  
##  <a name="iconnectionpointimpl__unadvise"></a>  IConnectionPointImpl::Unadvise  
 Terminates a connection previously established through [Advise](../vs140/IConnectionPointImpl--Advise.md).  
  
```  
  
STDMETHOD(Unadvise)(  
      DWORD  dwCookie  
   );  
  
```  
  
### Remarks  
 See [IConnectionPoint::Unadvise](http://msdn.microsoft.com/library/windows/desktop/ms686608) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [IConnectionPoint](http://msdn.microsoft.com/library/windows/desktop/ms694318)   
 [Class Overview](../vs140/ATL-Class-Overview.md)