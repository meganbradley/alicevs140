---
title: "CBindStatusCallback Class"
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
ms.assetid: 0f5da276-6031-4418-b2a9-a4750ef29e77
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback Class
This class implements the `IBindStatusCallback` interface.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template <class  T  
   , int  nBindFlags  
   = BINDF_ASYNCHRONOUS |   
   BINDF_ASYNCSTORAGE | BINDF_GETNEWESTVERSION | BINDF_NOWRITECACHE>  
   class ATL_NO_VTABLE CBindStatusCallback : public CComObjectRootEx  
   < T  
   ::_ThreadModel::ThreadModelNoCS>, public IBindStatusCallbackImpl< T  
   >  
  
```  
  
#### Parameters  
 `T`  
 Your class containing the function that will be called as the data is received.  
  
 *nBindFlags*  
 Specifies the bind flags that are returned by [GetBindInfo](../vs140/CBindStatusCallback--GetBindInfo.md). The default implementation sets the binding to be asynchronous, retrieves the newest version of the data/object, and does not store retrieved data in the disk cache.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CBindStatusCallback::CBindStatusCallback](../vs140/CBindStatusCallback--CBindStatusCallback.md)|The constructor.|  
|[CBindStatusCallback::~CBindStatusCallback](../vs140/CBindStatusCallback--~CBindStatusCallback.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CBindStatusCallback::Download](../vs140/CBindStatusCallback--Download.md)|Static method that starts the download process, creates a `CBindStatusCallback` object, and calls `StartAsyncDownload`.|  
|[CBindStatusCallback::GetBindInfo](../vs140/CBindStatusCallback--GetBindInfo.md)|Called by the asynchronous moniker to request information on the type of bind to be created.|  
|[CBindStatusCallback::GetPriority](../vs140/CBindStatusCallback--GetPriority.md)|Called by the asynchronous moniker to get the priority of the bind operation. The ATL implementation returns `E_NOTIMPL`.|  
|[CBindStatusCallback::OnDataAvailable](../vs140/CBindStatusCallback--OnDataAvailable.md)|Called to provide data to your application as it becomes available. Reads the data, then calls the function passed to it to use the data.|  
|[CBindStatusCallback::OnLowResource](../vs140/CBindStatusCallback--OnLowResource.md)|Called when resources are low. The ATL implementation returns `S_OK`.|  
|[CBindStatusCallback::OnObjectAvailable](../vs140/CBindStatusCallback--OnObjectAvailable.md)|Called by the asynchronous moniker to pass an object interface pointer to your application. The ATL implementation returns `S_OK`.|  
|[CBindStatusCallback::OnProgress](../vs140/CBindStatusCallback--OnProgress.md)|Called to indicate the progress of a data downloading process. The ATL implementation returns `S_OK`.|  
|[CBindStatusCallback::OnStartBinding](../vs140/CBindStatusCallback--OnStartBinding.md)|Called when binding is started.|  
|[CBindStatusCallback::OnStopBinding](../vs140/CBindStatusCallback--OnStopBinding.md)|Called when the asynchronous data transfer is stopped.|  
|[CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)|Initializes the bytes available and bytes read to zero, creates a push-type stream object from a URL, and calls `OnDataAvailable` every time data is available.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CBindStatusCallback::m_dwAvailableToRead](../vs140/CBindStatusCallback--m_dwAvailableToRead.md)|Number of bytes available to read.|  
|[CBindStatusCallback::m_dwTotalRead](../vs140/CBindStatusCallback--m_dwTotalRead.md)|Total number of bytes read.|  
|[CBindStatusCallback::m_pFunc](../vs140/CBindStatusCallback--m_pFunc.md)|Pointer to the function called when data is available.|  
|[CBindStatusCallback::m_pT](../vs140/CBindStatusCallback--m_pT.md)|Pointer to the object requesting the asynchronous data transfer.|  
|[CBindStatusCallback::m_spBindCtx](../vs140/CBindStatusCallback--m_spBindCtx.md)|Pointer to the [IBindCtx](http://msdn.microsoft.com/library/windows/desktop/ms693755) interface for the current bind operation.|  
|[CBindStatusCallback::m_spBinding](../vs140/CBindStatusCallback--m_spBinding.md)|Pointer to the `IBinding` interface for the current bind operation.|  
|[CBindStatusCallback::m_spMoniker](../vs140/CBindStatusCallback--m_spMoniker.md)|Pointer to the [IMoniker](http://msdn.microsoft.com/library/windows/desktop/ms679705) interface for the URL to use.|  
|[CBindStatusCallback::m_spStream](../vs140/CBindStatusCallback--m_spStream.md)|Pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface for the data transfer.|  
  
## Remarks  
 The `CBindStatusCallback` class implements the `IBindStatusCallback` interface. `IBindStatusCallback` must be implemented by your application so it can receive notifications from an asynchronous data transfer. The asynchronous moniker provided by the system uses `IBindStatusCallback` methods to send and receive information about the asynchronous data transfer to and from your object.  
  
 Typically, the `CBindStatusCallback` object is associated with a specific bind operation. For example, in the [ASYNC](../vs140/Visual-C---Samples.md) sample, when you set the URL property, it creates a `CBindStatusCallback` object in the call to `Download`:  
  
 [!CODE [NVC_ATL_Windowing#86](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#86)]  
  
 The asynchronous moniker uses the callback function `OnData` to call your application when it has data. The asynchronous moniker is provided by the system.  
  
## Inheritance Hierarchy  
 `CComObjectRootBase`  
  
 `IBindStatusCallback`  
  
 [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md)  
  
 `CBindStatusCallback`  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="cbindstatuscallback__cbindstatuscallback"></a>  CBindStatusCallback::CBindStatusCallback  
 The constructor.  
  
```  
  
CBindStatusCallback(  
   );  
  
```  
  
### Remarks  
 Creates an object to receive notifications concerning the asynchronous data transfer. Typically, one object is created for each bind operation.  
  
 The constructor also initializes [m_pT](../vs140/CBindStatusCallback--m_pT.md) and [m_pFunc](../vs140/CBindStatusCallback--m_pFunc.md) to **NULL**.  
  
##  <a name="cbindstatuscallback___dtorcbindstatuscallback"></a>  CBindStatusCallback::~CBindStatusCallback  
 The destructor.  
  
```  
  
~CBindStatusCallback( );  
  
```  
  
### Remarks  
 Frees all allocated resources.  
  
##  <a name="cbindstatuscallback__download"></a>  CBindStatusCallback::Download  
 Creates a `CBindStatusCallback` object and calls `StartAsyncDownload` to start downloading data asynchronously from the specified URL.  
  
```  
  
static HRESULT Download( T  
   *  pT,  
   ATL_PDATAAVAILABLE  pFunc,  
   BSTR  bstrURL,  
   IUnknown*  pUnkContainer =                 NULL,  
   BOOL  bRelative =                 FALSE  
   );  
  
```  
  
### Parameters  
 *pT*  
 [in] A pointer to the object requesting the asynchronous data transfer. The `CBindStatusCallback` object is templatized on this object's class.  
  
 *pFunc*  
 [in] A pointer to the function that receives the data that is read. The function is a member of your object's class of type `T`. See [StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md) for syntax and an example.  
  
 `bstrURL`  
 [in] The URL to obtain data from. Can be any valid URL or file name. Cannot be **NULL**. For example:  
  
 `CComBSTR mybstr =_T("http://somesite/data.htm")`  
  
 `pUnkContainer`  
 [in] The **IUnknown** of the container. **NULL** by default.  
  
 `bRelative`  
 [in] A flag indicating whether the URL is relative or absolute. **FALSE** by default, meaning the URL is absolute.  
  
### Return Value  
 One of the standard `HRESULT` values.  
  
### Remarks  
 Every time data is available it is sent to the object through `OnDataAvailable`. `OnDataAvailable` reads the data and calls the function pointed to by *pFunc* (for example, to store the data or print it to the screen).  
  
##  <a name="cbindstatuscallback__getbindinfo"></a>  CBindStatusCallback::GetBindInfo  
 Called to tell the moniker how to bind.  
  
```  
  
STDMETHOD(GetBindInfo)(  
      DWORD*  pgrfBSCF,  
   BINDINFO*  pbindinfo  
   );  
  
```  
  
### Parameters  
 *pgrfBSCF*  
 [out] A pointer to **BINDF** enumeration values indicating how the bind operation should occur. By default, set with the following enumeration values:  
  
 **BINDF_ASYNCHRONOUS** Asynchronous download.  
  
 **BINDF_ASYNCSTORAGE** `OnDataAvailable` returns **E_PENDING** when data is not yet available rather than blocking until data is available.  
  
 **BINDF_GETNEWESTVERSION** The bind operation should retrieve the newest version of the data.  
  
 **BINDF_NOWRITECACHE** The bind operation should not store retrieved data in the disk cache.  
  
 *pbindinfo*  
 [in, out] A pointer to the **BINDINFO** structure giving more information about how the object wants binding to occur.  
  
### Return Value  
 One of the standard `HRESULT` values.  
  
### Remarks  
 The default implementation sets the binding to be asynchronous and to use the data-push model. In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.  
  
##  <a name="cbindstatuscallback__getpriority"></a>  CBindStatusCallback::GetPriority  
 Called by the asynchronous moniker to get the priority of the bind operation.  
  
```  
  
STDMETHOD(GetPriority)(  
      LONG*  pnPriority  
   );  
  
```  
  
### Parameters  
 *pnPriority*  
 [out] Address of the **LONG** variable that, on success, receives the priority.  
  
### Return Value  
 Returns **E_NOTIMPL**.  
  
##  <a name="cbindstatuscallback__m_dwavailabletoread"></a>  CBindStatusCallback::m_dwAvailableToRead  
 Can be used to store the number of bytes available to be read.  
  
```  
  
DWORD m_dwAvailableToRead;  
  
```  
  
### Remarks  
 Initialized to zero in `StartAsyncDownload`.  
  
##  <a name="cbindstatuscallback__m_dwtotalread"></a>  CBindStatusCallback::m_dwTotalRead  
 The cumulative total of bytes read in the asynchronous data transfer.  
  
```  
  
DWORD m_dwTotalRead;  
  
```  
  
### Remarks  
 Incremented every time `OnDataAvailable` is called by the number of bytes actually read. Initialized to zero in `StartAsyncDownload`.  
  
##  <a name="cbindstatuscallback__m_pfunc"></a>  CBindStatusCallback::m_pFunc  
 The function pointed to by `m_pFunc` is called by `OnDataAvailable` after it reads the available data (for example, to store the data or print it to the screen).  
  
```  
  
ATL_PDATAAVAILABLE m_pFunc;  
  
```  
  
### Remarks  
 The function pointed to by `m_pFunc` is a member of your object's class and has the following syntax:  
  
 `void Function_Name(`  
  
 `CBindStatusCallback<T>* pbsc,`  
  
 `BYTE* pBytes,`  
  
 `DWORD dwSize`  
  
 `);`  
  
##  <a name="cbindstatuscallback__m_pt"></a>  CBindStatusCallback::m_pT  
 A pointer to the object requesting the asynchronous data transfer.  
  
```  
T  
  * m_pT;  
  
```  
  
### Remarks  
 The `CBindStatusCallback` object is templatized on this object's class.  
  
##  <a name="cbindstatuscallback__m_spbindctx"></a>  CBindStatusCallback::m_spBindCtx  
 A pointer to an [IBindCtx](http://msdn.microsoft.com/library/windows/desktop/ms693755) interface that provides access to the bind context (an object that stores information about a particular moniker binding operation).  
  
```  
  
CComPtr<IBindCtx> m_spBindCtx;  
  
```  
  
### Remarks  
 Initialized in `StartAsyncDownload`.  
  
##  <a name="cbindstatuscallback__m_spbinding"></a>  CBindStatusCallback::m_spBinding  
 A pointer to the `IBinding` interface of the current bind operation.  
  
```  
  
CComPtr<IBinding> m_spBinding;  
  
```  
  
### Remarks  
 Initialized in `OnStartBinding` and released in `OnStopBinding`.  
  
##  <a name="cbindstatuscallback__m_spmoniker"></a>  CBindStatusCallback::m_spMoniker  
 A pointer to the [IMoniker](http://msdn.microsoft.com/library/windows/desktop/ms679705) interface for the URL to use.  
  
```  
  
CComPtr<IMoniker> m_spMoniker;  
  
```  
  
### Remarks  
 Initialized in `StartAsyncDownload`.  
  
##  <a name="cbindstatuscallback__m_spstream"></a>  CBindStatusCallback::m_spStream  
 A pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface of the current bind operation.  
  
```  
  
CComPtr<IStream> m_spStream;  
  
```  
  
### Remarks  
 Initialized in `OnDataAvailable` from the **STGMEDIUM** structure when the **BCSF** flag is **BCSF_FIRSTDATANOTIFICATION** and released when the **BCSF** flag is **BCSF_LASTDATANOTIFICATION**.  
  
##  <a name="cbindstatuscallback__ondataavailable"></a>  CBindStatusCallback::OnDataAvailable  
 The system-supplied asynchronous moniker calls `OnDataAvailable` to provide data to the object as it becomes available.  
  
```  
  
STDMETHOD(OnDataAvailable)(  
      DWORD  grfBSCF,  
   DWORD  dwSize,  
   FORMATETC*  /* pformatetc */,  
   STGMEDIUM*  pstgmed  
   );  
  
```  
  
### Parameters  
 *grfBSCF*  
 [in] A **BSCF** enumeration value. One or more of the following:                                 **BSCF_FIRSTDATANOTIFICATION**,                                 **BSCF_INTERMEDIARYDATANOTIFICATION**, or **BSCF_LASTDATANOTIFICATION**.  
  
 `dwSize`  
 [in] The cumulative amount (in bytes) of data available since the beginning of the binding. Can be zero, indicating that the amount of data is not relevant or that no specific amount became available.  
  
 *pformatetc*  
 [in] Pointer to the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682242) structure that contains the format of the available data. If there is no format, can be **CF_NULL**.  
  
 *pstgmed*  
 [in] Pointer to the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms695269) structure that holds the actual data now available.  
  
### Return Value  
 One of the standard `HRESULT` values.  
  
### Remarks  
 `OnDataAvailable` reads the data, then calls a method of your object's class (for example, to store the data or print it to the screen). See [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md) for details.  
  
##  <a name="cbindstatuscallback__onlowresource"></a>  CBindStatusCallback::OnLowResource  
 Called when resources are low.  
  
```  
  
STDMETHOD(OnLowResource)(  
      DWORD  /* dwReserved */  
   );  
  
```  
  
### Parameters  
 `dwReserved`  
 Reserved.  
  
### Return Value  
 Returns `S_OK`.  
  
##  <a name="cbindstatuscallback__onobjectavailable"></a>  CBindStatusCallback::OnObjectAvailable  
 Called by the asynchronous moniker to pass an object interface pointer to your application.  
  
```  
  
STDMETHOD(OnObjectAvailable)(  
      REFID  /* riid */,  
   IUnknown*  /* punk */   
   );  
  
```  
  
### Parameters  
 `riid`  
 Interface identifier of the requested interface. Unused.  
  
 `punk`  
 Address of the IUnknown interface. Unused.  
  
### Return Value  
 Returns `S_OK`.  
  
##  <a name="cbindstatuscallback__onprogress"></a>  CBindStatusCallback::OnProgress  
 Called to indicate the progress of a data downloading process.  
  
```  
  
STDMETHOD(OnProgress)(  
      ULONG  /* ulProgress */,  
   ULONG  /* ulProgressMax */,  
   ULONG  /* ulStatusCode */,  
   LPCWSTRONG  /* szStatusText */   
   );  
  
```  
  
### Parameters  
 `ulProgress`  
 Unsigned long integer. Unused.  
  
 `ulProgressMax`  
 Unsigned long integer Unused.  
  
 `ulStatusCode`  
 Unsigned long integer. Unused.  
  
 `szStatusText`  
 Address of a string value. Unused.  
  
### Return Value  
 Returns `S_OK`.  
  
##  <a name="cbindstatuscallback__onstartbinding"></a>  CBindStatusCallback::OnStartBinding  
 Sets the data member [m_spBinding](../vs140/CBindStatusCallback--m_spBinding.md) to the `IBinding` pointer in `pBinding`.  
  
```  
  
STDMETHOD(OnStartBinding)(  
      DWORD  /* dwReserved */,  
   IBinding*  pBinding  
   );  
  
```  
  
### Parameters  
 `dwReserved`  
 Reserved for future use.  
  
 `pBinding`  
 [in] Address of the IBinding interface of the current bind operation. This cannot be NULL. The client should call AddRef on this pointer to keep a reference to the binding object.  
  
##  <a name="cbindstatuscallback__onstopbinding"></a>  CBindStatusCallback::OnStopBinding  
 Releases the `IBinding` pointer in the data member [m_spBinding](../vs140/CBindStatusCallback--m_spBinding.md).  
  
```  
  
STDMETHOD(OnStopBinding)(  
      HRESULT  hresult,  
   LPCWSTR  /* szError */   
   );  
  
```  
  
### Parameters  
 `hresult`  
 Status code returned from the bind operation.  
  
 szStatusText  
 Address of a string value Unused.  
  
### Remarks  
 Called by the system-supplied asynchronous moniker to indicate the end of the bind operation.  
  
##  <a name="cbindstatuscallback__startasyncdownload"></a>  CBindStatusCallback::StartAsyncDownload  
 Starts downloading data asynchronously from the specified URL.  
  
```  
  
HRESULT StartAsyncDownload( T  
   *  pT,  
   ATL_PDATAAVAILABLE  pFunc,  
   BSTR  bstrURL,  
      IUnknown*  pUnkContainer  
    = NULL,  
   BOOL  bRelative =                 FALSE  
   );  
  
```  
  
### Parameters  
 *pT*  
 [in] A pointer to the object requesting the asynchronous data transfer. The `CBindStatusCallback` object is templatized on this object's class.  
  
 *pFunc*  
 [in] A pointer to the function that receives the data being read. The function is a member of your object's class of type `T`. See **Remarks** for syntax and an example.  
  
 `bstrURL`  
 [in] The URL to obtain data from. Can be any valid URL or file name. Cannot be **NULL**. For example:  
  
 `CComBSTR mybstr =_T("http://somesite/data.htm")`  
  
 `pUnkContainer`  
 [in] The **IUnknown** of the container. **NULL** by default.  
  
 `bRelative`  
 [in] A flag indicating whether the URL is relative or absolute. **FALSE** by default, meaning the URL is absolute.  
  
### Return Value  
 One of the standard `HRESULT` values.  
  
### Remarks  
 Every time data is available it is sent to the object through `OnDataAvailable`. `OnDataAvailable` reads the data and calls the function pointed to by *pFunc* (for example, to store the data or print it to the screen).  
  
 The function pointed to by *pFunc* is a member of your object's class and has the following syntax:  
  
 `void Function_Name(`  
  
 `CBindStatusCallback<T>*`  `pbsc` `,`  
  
 `BYTE*`  `pBytes` `,`  
  
 `DWORD`  `dwSize`  
  
 `);`  
  
 In the following example (taken from the [ASYNC](../vs140/Visual-C---Samples.md) sample), the function `OnData` writes the received data into a text box.  
  
### Example  
 [!CODE [NVC_ATL_Windowing#87](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#87)]  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)