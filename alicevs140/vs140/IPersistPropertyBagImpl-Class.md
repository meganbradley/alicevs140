---
title: "IPersistPropertyBagImpl Class"
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
ms.assetid: 712af24d-99f8-40f2-9811-53b3ff6e5b19
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistPropertyBagImpl Class
This class implements **IUnknown** and allows an object to save its properties to a client-supplied property bag.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template <   
   class  T>  
   class ATL_NO_VTABLE IPersistPropertyBagImpl :  
   public IPersistPropertyBag  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IPersistPropertyBagImpl`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IPersistPropertyBagImpl::GetClassID](../vs140/IPersistPropertyBagImpl--GetClassID.md)|Retrieves the object's CLSID.|  
|[IPersistPropertyBagImpl::InitNew](../vs140/IPersistPropertyBagImpl--InitNew.md)|Initializes a newly created object. The ATL implementation returns `S_OK`.|  
|[IPersistPropertyBagImpl::Load](../vs140/IPersistPropertyBagImpl--Load.md)|Loads the object's properties from a client-supplied property bag.|  
|[IPersistPropertyBagImpl::Save](../vs140/IPersistPropertyBagImpl--Save.md)|Saves the object's properties into a client-supplied property bag.|  
  
## Remarks  
 The [IPersistPropertyBag](https://msdn.microsoft.com/en-us/library/aa768205.aspx) interface allows an object to save its properties to a client-supplied property bag. Class `IPersistPropertyBagImpl` provides a default implementation of this interface and implements **IUnknown** by sending information to the dump device in debug builds.  
  
 **IPersistPropertyBag** works in conjunction with [IPropertyBag](https://msdn.microsoft.com/en-us/library/aa768196.aspx) and [IErrorLog](https://msdn.microsoft.com/en-us/library/aa768231.aspx). These latter two interfaces must be implemented by the client. Through `IPropertyBag`, the client saves and loads the object's individual properties. Through **IErrorLog**, both the object and the client can report any errors encountered.  
  
 **Related Articles** [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md), [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
  
## Inheritance Hierarchy  
 `IPersistPropertyBag`  
  
 `IPersistPropertyBagImpl`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ipersistpropertybagimpl__getclassid"></a>  IPersistPropertyBagImpl::GetClassID  
 Retrieves the object's CLSID.  
  
```  
  
STDMETHOD(GetClassID)(  
      CLSID * pClassID  
   );  
  
```  
  
### Remarks  
 See [IPersist::GetClassID](http://msdn.microsoft.com/library/windows/desktop/ms688664) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersistpropertybagimpl__initnew"></a>  IPersistPropertyBagImpl::InitNew  
 Initializes a newly created object.  
  
```  
  
STDMETHOD(InitNew)( );  
  
```  
  
### Return Value  
 Returns `S_OK`.  
  
### Remarks  
 See [IPersistPropertyBag::InitNew](https://msdn.microsoft.com/en-us/library/aa768204.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersistpropertybagimpl__load"></a>  IPersistPropertyBagImpl::Load  
 Loads the object's properties from a client-supplied property bag.  
  
```  
  
STDMETHOD(Load)(  
      LPPROPERTYBAG  pPropBag,  
      LPERRORLOG  pErrorLog  
   );  
  
```  
  
### Remarks  
 ATL uses the object's property map to retrieve this information.  
  
 See [IPersistPropertyBag::Load](https://msdn.microsoft.com/en-us/library/aa768206.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ipersistpropertybagimpl__save"></a>  IPersistPropertyBagImpl::Save  
 Saves the object's properties into a client-supplied property bag.  
  
```  
  
STDMETHOD(Save)(  
      LPPROPERTYBAG  pPropBag,  
      BOOL  fClearDirty,  
      BOOL  fSaveAllProperties  
   );  
  
```  
  
### Remarks  
 ATL uses the object's property map to store this information. By default, this method saves all properties, regardless of the value of *fSaveAllProperties*.  
  
 See [IPersistPropertyBag::Save](https://msdn.microsoft.com/en-us/library/aa768207.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)