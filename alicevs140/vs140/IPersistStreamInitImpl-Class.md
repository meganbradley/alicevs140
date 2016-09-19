---
title: "IPersistStreamInitImpl Class"
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
ms.assetid: ef217c3c-020f-4cf8-871e-ef68e57865b8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistStreamInitImpl Class
This class implements **IUnknown** and provides a default implementation of the [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interface.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template<  
   class  T>  
   class ATL_NO_VTABLE IPersistStreamInitImpl :  
   public IPersistStreamInit  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IPersistStreamInitImpl`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IPersistStreamInitImpl::GetClassID](../vs140/IPersistStreamInitImpl--GetClassID.md)|Retrieves the object's CLSID.|  
|[IPersistStreamInitImpl::GetSizeMax](../vs140/IPersistStreamInitImpl--GetSizeMax.md)|Retrieves the size of the stream needed to save the object's data. The ATL implementation returns **E_NOTIMPL**.|  
|[IPersistStreamInitImpl::InitNew](../vs140/IPersistStreamInitImpl--InitNew.md)|Initializes a newly created object.|  
|[IPersistStreamInitImpl::IsDirty](../vs140/IPersistStreamInitImpl--IsDirty.md)|Checks whether the object's data has changed since it was last saved.|  
|[IPersistStreamInitImpl::Load](../vs140/IPersistStreamInitImpl--Load.md)|Loads the object's properties from the specified stream.|  
|[IPersistStreamInitImpl::Save](../vs140/IPersistStreamInitImpl--Save.md)|Saves the object's properties to the specified stream.|  
  
## Remarks  
 The [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interface allows a client to request that your object loads and saves its persistent data to a single stream. Class `IPersistStreamInitImpl` provides a default implementation of this interface and implements **IUnknown** by sending information to the dump device in debug builds.  
  
 **Related Articles** [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md), [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
  
## Inheritance Hierarchy  
 `IPersistStreamInit`  
  
 `IPersistStreamInitImpl`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ipersiststreaminitimpl__getclassid"></a>  IPersistStreamInitImpl::GetClassID  
 Retrieves the object's CLSID.  
  
```  
  
STDMETHOD(GetClassID)(  
      CLSID * pClassID  
   );  
  
```  
  
### Remarks  
 See [IPersist::GetClassID](http://msdn.microsoft.com/library/windows/desktop/ms688664) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersiststreaminitimpl__getsizemax"></a>  IPersistStreamInitImpl::GetSizeMax  
 Retrieves the size of the stream needed to save the object's data.  
  
```  
  
STDMETHOD(GetSizeMax)(  
      ULARGE_INTEGER FAR*  pcbSize  
   );  
  
```  
  
### Return Value  
 Returns **E_NOTIMPL**.  
  
### Remarks  
 See [IPersistStreamInit::GetSizeMax](http://msdn.microsoft.com/library/windows/desktop/ms687287) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersiststreaminitimpl__initnew"></a>  IPersistStreamInitImpl::InitNew  
 Initializes a newly created object.  
  
```  
  
STDMETHOD(InitNew)( );  
  
```  
  
### Remarks  
 See [IPersistStreamInit::InitNew](http://msdn.microsoft.com/library/windows/desktop/ms690234) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersiststreaminitimpl__isdirty"></a>  IPersistStreamInitImpl::IsDirty  
 Checks whether the object's data has changed since it was last saved.  
  
```  
  
STDMETHOD(IsDirty)( );  
  
```  
  
### Remarks  
 See [IPersistStreamInit::IsDirty](http://msdn.microsoft.com/library/windows/desktop/ms680092) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersiststreaminitimpl__load"></a>  IPersistStreamInitImpl::Load  
 Loads the object's properties from the specified stream.  
  
```  
  
STDMETHOD(Load)(  
      LPSTREAM  pStm  
   );  
  
```  
  
### Remarks  
 ATL uses the object's property map to retrieve this information.  
  
 See [IPersistStreamInit::Load](http://msdn.microsoft.com/library/windows/desktop/ms680730) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersiststreaminitimpl__save"></a>  IPersistStreamInitImpl::Save  
 Saves the object's properties to the specified stream.  
  
```  
  
STDMETHOD(Save)(  
      LPSTREAM  pStm,  
      BOOL  fClearDirty  
   );  
  
```  
  
### Remarks  
 ATL uses the object's property map to store this information.  
  
 See [IPersistStreamInit::Save](http://msdn.microsoft.com/library/windows/desktop/ms694439) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Storages and Streams](http://msdn.microsoft.com/library/windows/desktop/aa380352)   
 [Class Overview](../vs140/ATL-Class-Overview.md)