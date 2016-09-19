---
title: "IObjectWithSiteImpl Class"
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
ms.assetid: 4e1f774f-bc3d-45ee-9a1c-c3533a511588
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IObjectWithSiteImpl Class
This class provides methods allowing an object to communicate with its site.  
  
## Syntax  
  
```  
  
template<  
      class  T>  
   class ATL_NO_VTABLE IObjectWithSiteImpl :  
      public IObjectWithSite  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IObjectWithSiteImpl`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IObjectWithSiteImpl::GetSite](../vs140/IObjectWithSiteImpl--GetSite.md)|Queries the site for an interface pointer.|  
|[IObjectWithSiteImpl::SetChildSite](../vs140/IObjectWithSiteImpl--SetChildSite.md)|Provides the object with the site's **IUnknown** pointer.|  
|[IObjectWithSiteImpl::SetSite](../vs140/IObjectWithSiteImpl--SetSite.md)|Provides the object with the site's **IUnknown** pointer.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[IObjectWithSiteImpl::m_spUnkSite](../vs140/IObjectWithSiteImpl--m_spUnkSite.md)|Manages the site's **IUnknown** pointer.|  
  
## Remarks  
 The [IObjectWithSite](http://msdn.microsoft.com/library/windows/desktop/ms693765) interface allows an object to communicate with its site. Class `IObjectWithSiteImpl` provides a default implementation of this interface and implements **IUnknown** by sending information to the dump device in debug builds.  
  
 `IObjectWithSiteImpl` specifies two methods. The client first calls `SetSite`, passing the site's **IUnknown** pointer. This pointer is stored within the object, and can later be retrieved through a call to `GetSite`.  
  
 Typically, you derive your class from `IObjectWithSiteImpl` when you are creating an object that is not a control. For controls, derive your class from [IOleObjectImpl](../vs140/IOleObjectImpl-Class.md), which also provides a site pointer. Do not derive your class from both `IObjectWithSiteImpl` and `IOleObjectImpl`.  
  
## Inheritance Hierarchy  
 `IObjectWithSite`  
  
 `IObjectWithSiteImpl`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="iobjectwithsiteimpl__getsite"></a>  IObjectWithSiteImpl::GetSite  
 Queries the site for a pointer to the interface identified by `riid`.  
  
```  
  
STDMETHOD(GetSite)(  
      REFIID  riid,  
      void ** ppvSite  
   );  
  
```  
  
### Remarks  
 If the site supports this interface, the pointer is returned via `ppvSite`. Otherwise, `ppvSite` is set to **NULL**.  
  
 See [IObjectWithSite::GetSite](http://msdn.microsoft.com/library/windows/desktop/ms694452) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iobjectwithsiteimpl__m_spunksite"></a>  IObjectWithSiteImpl::m_spUnkSite  
 Manages the site's **IUnknown** pointer.  
  
```  
  
CComPtr< IUnknown > m_spUnkSite;  
  
```  
  
### Remarks  
 `m_spUnkSite` initially receives this pointer through a call to [SetSite](../vs140/IObjectWithSiteImpl--SetSite.md).  
  
##  <a name="iobjectwithsiteimpl__setchildsite"></a>  IObjectWithSiteImpl::SetChildSite  
 Provides the object with the site's **IUnknown** pointer.  
  
```  
  
HRESULT SetChildSite(  
      IUnknown*  pUnkSite  
   );  
  
```  
  
### Parameters  
 *pUnkSite*  
 [in] Pointer to the **IUnknown** interface pointer of the site managing this object. If NULL, the object should call `IUnknown::Release` on any existing site at which point the object no longer knows its site.  
  
### Return Value  
 Returns `S_OK`.  
  
##  <a name="iobjectwithsiteimpl__setsite"></a>  IObjectWithSiteImpl::SetSite  
 Provides the object with the site's **IUnknown** pointer.  
  
```  
  
STDMETHOD(SetSite)(  
      IUnknown*  pUnkSite  
   );  
  
```  
  
### Remarks  
 See [IObjectWithSite::SetSite](http://msdn.microsoft.com/library/windows/desktop/ms683869) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)