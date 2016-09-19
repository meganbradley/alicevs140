---
title: "ATL Classes"
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
ms.topic: index-page 
ms.assetid: 7da42e2d-ac84-4506-92bd-502a86d68bdc
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Classes
The Active Template Library (ATL) includes the following classes. To find a particular class by category, see the [ATL Class Overview](../vs140/ATL-Class-Overview.md).  
  
|Class|Description|Header file|  
|-----------|-----------------|-----------------|  
|[CA2AEX](../vs140/CA2AEX-Class.md)|This class is used by the string conversion macros `CA2TEX` and `CT2AEX`, and the typedef **CA2A**.|atlconv.h|  
|[CA2CAEX](../vs140/CA2CAEX-Class.md)|This class is used by string conversion macros `CA2CTEX` and `CT2CAEX`, and the typedef **CA2CA**.|atlconv.h|  
|[CA2WEX](../vs140/CA2WEX-Class.md)|This class is used by the string conversion macros `CA2TEX`, `CA2CTEX`, `CT2WEX`, and `CT2CWEX`, and the typedef **CA2W**.|atlconv.h|  
|[CAccessToken](../vs140/CAccessToken-Class.md)|This class is a wrapper for an access token.|atlsecurity.h|  
|[CAcl](../vs140/CAcl-Class.md)|This class is a wrapper for an **ACL** (access-control list) structure.|atlsecurity.h|  
|[CAdapt](../vs140/CAdapt-Class.md)|This template is used to wrap classes that redefine the address-of operator to return something other than the address of the object.|atlcomcli.h|  
|[CAtlArray](../vs140/CAtlArray-Class.md)|This class implements an array object.|atlcoll.h|  
|[CAtlAutoThreadModule](../vs140/CAtlAutoThreadModule-Class.md)|This class implements a thread-pooled, apartment-model COM server.|atlbase.h|  
|[CAtlAutoThreadModuleT](../vs140/CAtlAutoThreadModuleT-Class.md)|This class provides methods for implementing a thread-pooled, apartment-model COM server.|atlbase.h|  
|[CAtlBaseModule](../vs140/CAtlBaseModule-Class.md)|This class is instantiated in every ATL project.|atlcore.h|  
|[CAtlComModule](../vs140/CAtlComModule-Class.md)|This class implements a COM server module.|atlbase.h|  
|[CAtlDebugInterfacesModule](../vs140/CAtlDebugInterfacesModule-Class.md)|This class provides support for debugging interfaces.|atlbase.h|  
|[CAtlDllModuleT](../vs140/CAtlDllModuleT-Class.md)|This class represents the module for a DLL.|atlbase.h|  
|[CAtlException](../vs140/CAtlException-Class.md)|This class defines an ATL exception.|atlexcept.h|  
|[CAtlExeModuleT](../vs140/CAtlExeModuleT-Class.md)|This class represents the module for an application.|atlbase.h|  
|[CAtlFile](../vs140/CAtlFile-Class.md)|This class provides a thin wrapper around the Windows file-handling API.|atlfile.h|  
|[CAtlFileMapping](../vs140/CAtlFileMapping-Class.md)|This class represents a memory-mapped file, adding a cast operator to the methods of [CAtlFileMappingBase](../vs140/CAtlFileMappingBase-Class.md).|atlfile.h|  
|[CAtlFileMappingBase](../vs140/CAtlFileMappingBase-Class.md)|This class represents a memory-mapped file.|atlfile.h|  
|[CAtlList](../vs140/CAtlList-Class.md)|This class provides methods for creating and managing a list object.|atlcoll.h|  
|[CAtlMap](../vs140/CAtlMap-Class.md)|This class provides methods for creating and managing a map object.|atlcoll.h|  
|[CAtlModule](../vs140/CAtlModule-Class.md)|This class provides methods used by several ATL module classes.|atlbase.h|  
|[CAtlModuleT](../vs140/CAtlModuleT-Class.md)|This class implements an ATL module.|atlbase.h|  
|[CAtlPreviewCtrlImpl](../vs140/CAtlPreviewCtrlImpl-Class.md)|This class is an ATL implementation of a window that is placed on a host window provided by the Shell for Rich Preview.|atlpreviewctrlimpl.h|  
|[CAtlServiceModuleT](../vs140/CAtlServiceModuleT-Class.md)|This class implements a service.|atlbase.h|  
|[CAtlTemporaryFile](../vs140/CAtlTemporaryFile-Class.md)|This class provides methods for the creation and use of a temporary file.|atlfile.h|  
|[CAtlTransactionManager](../vs140/CAtlTransactionManager-Class.md)|This class provides a wrapper to Kernel Transaction Manager (KTM) functions.|atltransactionmanager.h|  
|[CAtlWinModule](../vs140/CAtlWinModule-Class.md)|This class provides support for ATL windowing components.|atlbase.h|  
|[CAutoPtr](../vs140/CAutoPtr-Class.md)|This class represents a smart pointer object.|atlbase.h|  
|[CAutoPtrArray](../vs140/CAutoPtrArray-Class.md)|This class provides methods useful when constructing an array of smart pointers.|atlbase.h|  
|[CAutoPtrElementTraits](../vs140/CAutoPtrElementTraits-Class.md)|This class provides methods, static functions, and typedefs useful when creating collections of smart pointers.|atlcoll.h|  
|[CAutoPtrList](../vs140/CAutoPtrList-Class.md)|This class provides methods useful when constructing a list of smart pointers.|atlcoll.h|  
|[CAutoVectorPtr](../vs140/CAutoVectorPtr-Class.md)|This class represents a smart pointer object using vector new and delete operators.|atlbase.h|  
|[CAutoVectorPtrElementTraits](../vs140/CAutoVectorPtrElementTraits-Class.md)|This class provides methods, static functions, and typedefs useful when creating collections of smart pointers using vector new and delete operators.|atlcoll.h|  
|[CAxDialogImpl](../vs140/CAxDialogImpl-Class.md)|This class implements a dialog box (modal or modeless) that hosts ActiveX controls.|atlwin.h|  
|[CAxWindow](../vs140/CAxWindow-Class.md)|This class provides methods for manipulating a window hosting an ActiveX control.|atlwin.h|  
|[CAxWindow2T](../vs140/CAxWindow2T-Class.md)|This class provides methods for manipulating a window that hosts an ActiveX control and also has support for hosting licensed ActiveX controls.|atlwin.h|  
|[CBindStatusCallback](../vs140/CBindStatusCallback-Class.md)|This class implements the `IBindStatusCallback` interface.|atlctl.h|  
|[CComAggObject](../vs140/CComAggObject-Class.md)|This class implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) for an aggregated object.|atlcom.h|  
|[CComAllocator](../vs140/CComAllocator-Class.md)|This class provides methods for managing memory using COM memory routines.|atlbase.h|  
|[CComApartment](../vs140/CComApartment-Class.md)|This class provides support for managing an apartment in a thread-pooled EXE module.|atlbase.h|  
|[CComAutoCriticalSection](../vs140/CComAutoCriticalSection-Class.md)|This class provides methods for obtaining and releasing ownership of a critical section object.|atlcore.h|  
|[CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md)|As of ATL 7.0, `CComAutoThreadModule` is obsolete: see [ATL Modules](../vs140/ATL-Module-Classes.md) for more details.|atlbase.h|  
|[CComBSTR](../vs140/CComBSTR-Class.md)|This class is a wrapper for `BSTR`s.|atlbase.h|  
|[CComCachedTearOffObject](../vs140/CComCachedTearOffObject-Class.md)|This class implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) for a tear-off interface.|atlcom.h|  
|[CComClassFactory](../vs140/CComClassFactory-Class.md)|This class implements the [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364) interface.|atlcom.h|  
|[CComClassFactory2](../vs140/CComClassFactory2-Class.md)|This class implements the [IClassFactory2](http://msdn.microsoft.com/library/windows/desktop/ms692720) interface.|atlcom.h|  
|[CComClassFactoryAutoThread](../vs140/CComClassFactoryAutoThread-Class.md)|This class implements the [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364) interface and allows objects to be created in multiple apartments.|atlcom.h|  
|[CComClassFactorySingleton](../vs140/CComClassFactorySingleton-Class.md)|This class derives from [CComClassFactory](../vs140/CComClassFactory-Class.md) and uses [CComObjectGlobal](../vs140/CComObjectGlobal-Class.md) to construct a single object.|atlcom.h|  
|[CComCoClass](../vs140/CComCoClass-Class.md)|This class provides methods for creating instances of a class and obtaining its properties.|atlcom.h|  
|[CComCompositeControl](../vs140/CComCompositeControl-Class.md)|This class provides the methods required to implement a composite control.|atlctl.h|  
|[CComContainedObject](../vs140/CComContainedObject-Class.md)|This class implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) by delegating to the owner object's **IUnknown**.|atlcom.h|  
|[CComControl](../vs140/CComControl-Class.md)|This class provides methods for creating and managing ATL controls.|atlctl.h|  
|[CComControlBase](../vs140/CComControlBase-Class.md)|This class provides methods for creating and managing ATL controls.|atlctl.h|  
|[CComCriticalSection](../vs140/CComCriticalSection-Class.md)|This class provides methods for obtaining and releasing ownership of a critical section object.|atlcore.h|  
|[CComCritSecLock](../vs140/CComCritSecLock-Class.md)|This class provides methods for locking and unlocking a critical section object.|atlbase.h|  
|[CComCurrency](../vs140/CComCurrency-Class.md)|This class has methods and operators for creating and managing a `CURRENCY` object.|atlcur.h|  
|[CComDynamicUnkArray](../vs140/CComDynamicUnkArray-Class.md)|This class stores an array of **IUnknown** pointers.|atlcom.h|  
|[CComEnum](../vs140/CComEnum-Class.md)|This class defines a COM enumerator object based on an array.|atlcom.h|  
|[CComEnumImpl](../vs140/CComEnumImpl-Class.md)|This class provides the implementation for a COM enumerator interface where the items being enumerated are stored in an array.|atlcom.h|  
|[CComEnumOnSTL](../vs140/CComEnumOnSTL-Class.md)|This class defines a COM enumerator object based on an STL collection.|atlcom.h|  
|[CComFakeCriticalSection](../vs140/CComFakeCriticalSection-Class.md)|This class provides the same methods as [CComCriticalSection](../vs140/CComCriticalSection-Class.md) but does not provide a critical section.|atlcore.h|  
|[CComGITPtr](../vs140/CComGITPtr-Class.md)|This class provides methods for dealing with interface pointers and the global interface table (GIT).|atlbase.h|  
|[CComHeap](../vs140/CComHeap-Class.md)|This class implements [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md) using the COM memory allocation functions.|ATLComMem.h|  
|[CComHeapPtr](../vs140/CComHeapPtr-Class.md)|A smart pointer class for managing heap pointers.|atlbase.h|  
|[CComModule](../vs140/CComModule-Class.md)|As of ATL 7.0, `CComModule` is obsolete: see [ATL Modules](../vs140/ATL-Module-Classes.md) for more details.|atlbase.h|  
|[CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md)|This class provides thread-safe methods for incrementing and decrementing the value of a variable.|atlbase.h|  
|[CComMultiThreadModelNoCS](../vs140/CComMultiThreadModelNoCS-Class.md)|This class provides thread-safe methods for incrementing and decrementing the value of a variable, without critical section locking or unlocking functionality.|atlbase.h|  
|[CComObject](../vs140/CComObject-Class.md)|This class implements **IUnknown** for a nonaggregated object.|atlcom.h|  
|[CComObjectGlobal](../vs140/CComObjectGlobal-Class.md)|This class manages a reference count on the module containing your `Base` object.|atlcom.h|  
|[CComObjectNoLock](../vs140/CComObjectNoLock-Class.md)|This class implements **IUnknown** for a nonaggregated object, but does not increment the module lock count in the constructor.|atlcom.h|  
|[CComObjectRoot](../vs140/CComObjectRoot-Class.md)|This typedef of [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md) is templatized on the default threading model of the server.|atlcom.h|  
|[CComObjectRootEx](../vs140/CComObjectRootEx-Class.md)|This class provides methods to handle object reference count management for both nonaggregated and aggregated objects.|atlcom.h|  
|[CComObjectStack](../vs140/CComObjectStack-Class.md)|This class creates a temporary COM object and provides it with a skeletal implementation of **IUnknown**.|atlcom.h|  
|[CComPolyObject](../vs140/CComPolyObject-Class.md)|This class implements **IUnknown** for an aggregated or nonaggregated object.|atlcom.h|  
|[CComPtr](../vs140/CComPtr-Class.md)|A smart pointer class for managing COM interface pointers.|atlcomcli.h|  
|[CComPtrBase](../vs140/CComPtrBase-Class.md)|This class provides a basis for smart pointer classes using COM-based memory routines.|atlcomcli.h|  
|[CComQIPtr](../vs140/CComQIPtr-Class.md)|A smart pointer class for managing COM interface pointers.|atlcomcli.h|  
|[CComQIPtrElementTraits](../vs140/CComQIPtrElementTraits-Class.md)|This class provides methods, static functions, and typedefs useful when creating collections of COM interface pointers.|atlcoll.h|  
|[CComSafeArray](../vs140/CComSafeArray-Class.md)|This class is a wrapper for the `SAFEARRAY Data Type` structure.|atlsafe.h|  
|[CComSafeArrayBound](../vs140/CComSafeArrayBound-Class.md)|This class is a wrapper for a `SAFEARRAYBOUND` structure.|atlsafe.h|  
|[CComSimpleThreadAllocator](../vs140/CComSimpleThreadAllocator-Class.md)|This class manages thread selection for the class [CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md).|atlbase.h|  
|[CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md)|This class provides methods for incrementing and decrementing the value of a variable.|atlbase.h|  
|[CComTearOffObject](../vs140/CComTearOffObject-Class.md)|This class implements a tear-off interface.|atlcom.h|  
|[CComUnkArray](../vs140/CComUnkArray-Class.md)|This class stores **IUnknown** pointers and is designed to be used as a parameter to the [IConnectionPointImpl](../vs140/IConnectionPointImpl-Class.md) template class.|atlcom.h|  
|[CComVariant](../vs140/CComVariant-Class.md)|This class wraps the VARIANT type, providing a member indicating the type of data stored.|atlcomcli.h|  
|[CContainedWindowT](../vs140/CContainedWindowT-Class.md)|This class implements a window contained within another object.|atlwin.h|  
|[CCRTAllocator](../vs140/CCRTAllocator-Class.md)|This class provides methods for managing memory using CRT memory routines.|atlcore.h|  
|[CCRTHeap](../vs140/CCRTHeap-Class.md)|This class implements [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md) using the CRT heap functions.|atlmem.h|  
|[CDacl](../vs140/CDacl-Class.md)|This class is a wrapper for a DACL (discretionary access-control list) structure.|atlsecurity.h|  
|[CDebugReportHook Class](../vs140/CDebugReportHook-Class.md)|Use this class to send debug reports to a named pipe.|atlutil.h|  
|[CDefaultCharTraits](../vs140/CDefaultCharTraits-Class.md)|This class provides two static functions for converting characters between uppercase and lowercase.|atlcoll.h|  
|[CDefaultCompareTraits](../vs140/CDefaultCompareTraits-Class.md)|This class provides default element comparison functions.|atlcoll.h|  
|[CDefaultElementTraits](../vs140/CDefaultElementTraits-Class.md)|This class provides default methods and functions for a collection class.|atlcoll.h|  
|[CDefaultHashTraits](../vs140/CDefaultHashTraits-Class.md)|This class provides a static function for calculating hash values.|atlcoll.h|  
|[CDialogImpl](../vs140/CDialogImpl-Class.md)|This class provides methods for creating a modal or modeless dialog box.|atlwin.h|  
|[CDynamicChain](../vs140/CDynamicChain-Class.md)|This class provides methods supporting the dynamic chaining of message maps.|atlwin.h|  
|[CElementTraits](../vs140/CElementTraits-Class.md)|This class is used by collection classes to provide methods and functions for moving, copying, comparison, and hashing operations.|atlcoll.h|  
|[CElementTraitsBase](../vs140/CElementTraitsBase-Class.md)|This class provides default copy and move methods for a collection class.|atlcoll.h|  
|[CFirePropNotifyEvent](../vs140/CFirePropNotifyEvent-Class.md)|This class provides methods for notifying the container's sink regarding control property changes.|atlctl.h|  
|[CGlobalHeap](../vs140/CGlobalHeap-Class.md)|This class implements [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md) using the Win32 global heap functions.|atlmem.h|  
|[CHandle](../vs140/CHandle-Class.md)|This class provides methods for creating and using a handle object.|atlbase.h|  
|[CHeapPtr](../vs140/CHeapPtr-Class.md)|A smart pointer class for managing heap pointers.|atlcore.h|  
|[CHeapPtrBase](../vs140/CHeapPtrBase-Class.md)|This class forms the basis for several smart heap pointer classes.|atlcore.h|  
|[CHeapPtrElementTraits Class](../vs140/CHeapPtrElementTraits-Class.md)|This class provides methods, static functions, and typedefs useful when creating collections of heap pointers.|atlcoll.h|  
|[CHeapPtrList](../vs140/CHeapPtrList-Class.md)|This class provides methods useful when constructing a list of heap pointers.|atlcoll.h|  
|[CImage](../vs140/CImage-Class.md)|Provides enhanced bitmap support, including the ability to load and save images in JPEG, GIF, BMP, and Portable Network Graphics (PNG) formats.|atlimage.h|  
|[CInterfaceArray](../vs140/CInterfaceArray-Class.md)|This class provides methods useful when constructing an array of COM interface pointers.|atlcoll.h|  
|[CInterfaceList](../vs140/CInterfaceList-Class.md)|This class provides methods useful when constructing a list of COM interface pointers.|atlcoll.h|  
|[CLocalHeap](../vs140/CLocalHeap-Class.md)|This class implements [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md) using the Win32 local heap functions.|atlmem.h|  
|[CMessageMap](../vs140/CMessageMap-Class.md)|This class allows an object's message maps to be accessed by another object.|atlwin.h|  
|[CNonStatelessWorker Class](../vs140/CNonStatelessWorker-Class.md)|Receives requests from a thread pool and passes them on to a worker object that is created and destroyed on each request.|atlutil.h|  
|[CNoWorkerThread Class](../vs140/CNoWorkerThread-Class.md)|Use this class as the argument for the `MonitorClass` template parameter cache classes if you want to disable dynamic cache maintenance.|atlutil.h|  
|[CPathT](../vs140/CPathT-Class.md)|This class represents a path.|atlpath.h|  
|[CPrimitiveElementTraits](../vs140/CPrimitiveElementTraits-Class.md)|This class provides default methods and functions for a collection class composed of primitive data types.|atlcoll.h|  
|[CPrivateObjectSecurityDesc](../vs140/CPrivateObjectSecurityDesc-Class.md)|This class represents a private object security descriptor object.|atlsecurity.h|  
|[CRBMap](../vs140/CRBMap-Class.md)|This class represents a mapping structure, using a Red-Black binary tree.|atlcoll.h|  
|[CRBMultiMap](../vs140/CRBMultiMap-Class.md)|This class represents a mapping structure that allows each key to be associated with more than one value, using a Red-Black binary tree.|atlcoll.h|  
|[CRBTree](../vs140/CRBTree-Class.md)|This class provides methods for creating and utilizing a Red-Black tree.|atlcoll.h|  
|[CRegKey](../vs140/CRegKey-Class.md)|This class provides methods for manipulating entries in the system registry.|atlbase.h|  
|[CRTThreadTraits](../vs140/CRTThreadTraits-Class.md)|This class provides the creation function for a CRT thread. Use this class if the thread will use CRT functions.|atlbase.h|  
|[CSacl](../vs140/CSacl-Class.md)|This class is a wrapper for a SACL (system access-control list) structure.|atlsecurity.h|  
|[CSecurityAttributes](../vs140/CSecurityAttributes-Class.md)|This class is a thin wrapper for the **SECURITY_ATTRIBUTES** structure.|atlsecurity.h|  
|[CSecurityDesc](../vs140/CSecurityDesc-Class.md)|This class is a wrapper for the **SECURITY_DESCRIPTOR** structure.|atlsecurity.h|  
|[CSid](../vs140/CSid-Class.md)|This class is a wrapper for a `SID` (security identifier) structure.|atlsecurity.h|  
|[CSimpleArray](../vs140/CSimpleArray-Class.md)|This class provides methods for managing a simple array.|atlsimpcoll.h|  
|[CSimpleArrayEqualHelper](../vs140/CSimpleArrayEqualHelper-Class.md)|This class is a helper for the [CSimpleArray](../vs140/CSimpleArray-Class.md) class.|atlsimpcoll.h|  
|[CSimpleArrayEqualHelperFalse](../vs140/CSimpleArrayEqualHelperFalse-Class.md)|This class is a helper for the [CSimpleArray](../vs140/CSimpleArray-Class.md) class.|atlsimpcoll.h|  
|[CSimpleDialog](../vs140/CSimpleDialog-Class.md)|This class implements a basic modal dialog box.|atlwin.h|  
|[CSimpleMap](../vs140/CSimpleMap-Class.md)|This class provides support for a simple mapping array.|atlsimpcoll.h|  
|[CSimpleMapEqualHelper](../vs140/CSimpleMapEqualHelper-Class.md)|This class is a helper for the [CSimpleMap](../vs140/CSimpleMap-Class.md) class.|atlsimpcoll.h|  
|[CSimpleMapEqualHelperFalse](../vs140/CSimpleMapEqualHelperFalse-Class.md)|This class is a helper for the [CSimpleMap](../vs140/CSimpleMap-Class.md) class.|atlsimpcoll.h|  
|[CSnapInItemImpl](../Topic/CSnapInItemImpl%20Class.md)|This class provides methods for implementing a snap-in node object.|atlsnap.h|  
|[CSnapInPropertyPageImpl](../vs140/CSnapInPropertyPageImpl-Class.md)|This class provides methods for implementing a snap-in property page object.|atlsnap.h|  
|[CStockPropImpl](../vs140/CStockPropImpl-Class.md)|This class provides methods for supporting stock property values.|atlctl.h|  
|[CStringElementTraits](../vs140/CStringElementTraits-Class.md)|This class provides static functions used by collection classes storing `CString` objects.|cstringt.h|  
|[CStringElementTraitsI](../vs140/CStringElementTraitsI-Class.md)|This class provides static functions related to strings stored in collection class objects. It is similar to [CStringElementTraits](../vs140/CStringElementTraits-Class.md), but performs case-insensitive comparisons.|atlcoll.h|  
|[CStringRefElementTraits](../vs140/CStringRefElementTraits-Class.md)|This class provides static functions related to strings stored in collection class objects. The string objects are dealt with as references.|atlcoll.h|  
|[CThreadPool Class](../vs140/CThreadPool-Class.md)|This class provides a pool of worker threads that process a queue of work items.|atlutil.h|  
|[CTokenGroups](../vs140/CTokenGroups-Class.md)|This class is a wrapper for the **TOKEN_GROUPS** structure.|atlsecurity.h|  
|[CTokenPrivileges](../vs140/CTokenPrivileges-Class.md)|This class is a wrapper for the **TOKEN_PRIVILEGES** structure.|atlsecurity.h|  
|[CUrl](../vs140/CUrl-Class.md)|This class represents a URL. It allows you to manipulate each element of the URL independently of the others whether parsing an existing URL string or building a string from scratch.|atlutil.h|  
|[CW2AEX](../vs140/CW2AEX-Class.md)|This class is used by the string conversion macros `CT2AEX`, `CW2TEX`, `CW2CTEX`, and `CT2CAEX`, and the typedef **CW2A**.|atlconv.h|  
|[CW2CWEX](../vs140/CW2CWEX-Class.md)|This class is used by the string conversion macros `CW2CTEX` and `CT2CWEX`, and the typedef **CW2CW**.|atlconv.h|  
|[CW2WEX](../vs140/CW2WEX-Class.md)|This class is used by the string conversion macros `CW2TEX` and `CT2WEX`, and the typedef `CW2W`.|atlconv.h|  
|[CWin32Heap](../vs140/CWin32Heap-Class.md)|This class implements [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md) using the Win32 heap allocation functions.|atlmem.h|  
|[CWindow](../vs140/CWindow-Class.md)|This class provides methods for manipulating a window.|atlwin.h|  
|[CWindowImpl](../vs140/CWindowImpl-Class.md)|This class provides methods for creating or subclassing a window.|atlwin.h|  
|[CWinTraits](../vs140/CWinTraits-Class.md)|This class provides a method for standardizing the styles used when creating a window object.|atlwin.h|  
|[CWinTraitsOR](../vs140/CWinTraitsOR-Class.md)|This class provides a method for standardizing the styles used when creating a window object.|atlwin.h|  
|[CWndClassInfo](../vs140/CWndClassInfo-Class.md)|This class provides methods for registering information for a window class.|atlwin.h|  
|[CWorkerThread Class](../vs140/CWorkerThread-Class.md)|This class creates a worker thread or uses an existing one, waits on one or more kernel object handles, and executes a specified client function when one of the handles is signaled.|atlutil.h|  
|[IAtlAutoThreadModule](../vs140/IAtlAutoThreadModule-Class.md)|This class represents an interface to a `CreateInstance` method.|atlbase.h|  
|[IAtlMemMgr](../vs140/IAtlMemMgr-Class.md)|This class represents the interface to a memory manager.|atlmem.h|  
|[IAxWinAmbientDispatch](../vs140/IAxWinAmbientDispatch-Interface.md)|This interface provides methods for specifying characteristics of the hosted control or container.|atlbase.h, ATLIFace.h|  
|[IAxWinAmbientDispatchEx](../vs140/IAxWinAmbientDispatchEx-Interface.md)|This interface implements supplemental ambient properties for a hosted control.|atlbase.h, ATLIFace.h|  
|[IAxWinHostWindow](../vs140/IAxWinHostWindow-Interface.md)|This interface provides methods for manipulating a control and its host object.|atlbase.h, ATLIFace.h|  
|[IAxWinHostWindowLic](../vs140/IAxWinHostWindowLic-Interface.md)|This interface provides methods for manipulating a licensed control and its host object.|atlbase.h, ATLIFace.h|  
|[ICollectionOnSTLImpl](../vs140/ICollectionOnSTLImpl-Class.md)|This class provides methods used by a collection class.|atlcom.h|  
|[IConnectionPointContainerImpl](../vs140/IConnectionPointContainerImpl-Class.md)|This class implements a connection point container to manage a collection of [IConnectionPointImpl](../vs140/IConnectionPointImpl-Class.md) objects.|atlcom.h|  
|[IConnectionPointImpl](../vs140/IConnectionPointImpl-Class.md)|This class implements a connection point.|atlcom.h|  
|[IDataObjectImpl](../vs140/IDataObjectImpl-Class.md)|This class provides methods for supporting Uniform Data Transfer and managing connections.|atlctl.h|  
|[IDispatchImpl](../vs140/IDispatchImpl-Class.md)|This class provides a default implementation for the `IDispatch` portion of a dual interface.|atlcom.h|  
|[IDispEventImpl](../vs140/IDispEventImpl-Class.md)|This class provides implementations of the `IDispatch` methods.|atlcom.h|  
|[IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md)|This class provides implementations of the `IDispatch` methods, without getting type information from a type library.|atlcom.h|  
|[IDocHostUIHandlerDispatch](../vs140/IDocHostUIHandlerDispatch-Interface.md)|An interface to the Microsoft HTML parsing and rendering engine.|atlbase.h, ATLIFace.h|  
|[IEnumOnSTLImpl](../vs140/IEnumOnSTLImpl-Class.md)|This class defines an enumerator interface based on an STL collection.|atlcom.h|  
|[IObjectSafetyImpl](../vs140/IObjectSafetyImpl-Class.md)|This class provides a default implementation of the `IObjectSafety` interface to allow a client to retrieve and set an object's safety levels.|atlctl.h|  
|[IObjectWithSiteImpl](../vs140/IObjectWithSiteImpl-Class.md)|This class provides methods allowing an object to communicate with its site.|atlcom.h|  
|[IOleControlImpl](../vs140/IOleControlImpl-Class.md)|This class provides a default implementation of the **IOleControl** interface and implements **IUnknown**.|atlctl.h|  
|[IOleInPlaceActiveObjectImpl](../vs140/IOleInPlaceActiveObjectImpl-Class.md)|This class provides methods for assisting communication between an in-place control and its container.|atlctl.h|  
|[IOleInPlaceObjectWindowlessImpl](../vs140/IOleInPlaceObjectWindowlessImpl-Class.md)|This class implements **IUnknown** and provides methods that enable a windowless control to receive window messages and to participate in drag-and-drop operations.|atlctl.h|  
|[IOleObjectImpl](../vs140/IOleObjectImpl-Class.md)|This class implements **IUnknown** and is the principal interface through which a container communicates with a control.|atlctl.h|  
|[IPerPropertyBrowsingImpl](../vs140/IPerPropertyBrowsingImpl-Class.md)|This class implements **IUnknown** and allows a client to access the information in an object's property pages.|atlctl.h|  
|[IPersistPropertyBagImpl](../vs140/IPersistPropertyBagImpl-Class.md)|This class implements **IUnknown** and allows an object to save its properties to a client-supplied property bag.|atlcom.h|  
|[IPersistStorageImpl](../vs140/IPersistStorageImpl-Class.md)|This class implements the [IPersistStorage](http://msdn.microsoft.com/library/windows/desktop/ms679731) interface.|atlcom.h|  
|[IPersistStreamInitImpl](../vs140/IPersistStreamInitImpl-Class.md)|This class implements **IUnknown** and provides a default implementation of the [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interface.|atlcom.h|  
|[IPointerInactiveImpl](../vs140/IPointerInactiveImpl-Class.md)|This class implements **IUnknown** and the [IPointerInactive](http://msdn.microsoft.com/library/windows/desktop/ms693712) interface methods.|atlctl.h|  
|[IPropertyNotifySinkCP](../vs140/IPropertyNotifySinkCP-Class.md)|This class exposes the [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) interface as an outgoing interface on a connectable object.|atlctl.h|  
|[IPropertyPage2Impl](../vs140/IPropertyPage2Impl-Class.md)|This class implements **IUnknown** and inherits the default implementation of [IPropertyPageImpl](../vs140/IPropertyPageImpl-Class.md).|atlctl.h|  
|[IPropertyPageImpl](../vs140/IPropertyPageImpl-Class.md)|This class implements **IUnknown** and provides a default implementation of the [IPropertyPage](http://msdn.microsoft.com/library/windows/desktop/ms691246) interface.|atlctl.h|  
|[IProvideClassInfo2Impl](../vs140/IProvideClassInfo2Impl-Class.md)|This class provides a default implementation of the [IProvideClassInfo](http://msdn.microsoft.com/library/windows/desktop/ms687303) and [IProvideClassInfo2](http://msdn.microsoft.com/library/windows/desktop/ms693764) methods.|atlcom.h|  
|[IQuickActivateImpl](../vs140/IQuickActivateImpl-Class.md)|This class combines containers' control initialization into a single call.|atlctl.h|  
|[IRunnableObjectImpl](../vs140/IRunnableObjectImpl-Class.md)|This class implements **IUnknown** and provides a default implementation of the [IRunnableObject](http://msdn.microsoft.com/library/windows/desktop/ms692783) interface.|atlctl.h|  
|[IServiceProviderImpl](../vs140/IServiceProviderImpl-Class.md)|This class provides a default implementation of the `IServiceProvider` interface.|atlcom.h|  
|[ISpecifyPropertyPagesImpl](../vs140/ISpecifyPropertyPagesImpl-Class.md)|This class implements **IUnknown** and provides a default implementation of the [ISpecifyPropertyPages](http://msdn.microsoft.com/library/windows/desktop/ms695217) interface.|atlcom.h|  
|[ISupportErrorInfoImpl](../vs140/ISupportErrorInfoImpl-Class.md)|This class provides a default implementation of the `ISupportErrorInfo Interface` interface and can be used when only a single interface generates errors on an object.|atlcom.h|  
|[IThreadPoolConfig Interface](../vs140/IThreadPoolConfig-Interface.md)|This interface provides methods for configuring a thread pool.|atlutil.h|  
|[IViewObjectExImpl](../vs140/IViewObjectExImpl-Class.md)|This class implements **IUnknown** and provides default implementations of the [IViewObject](http://msdn.microsoft.com/library/windows/desktop/ms680763), [IViewObject2](http://msdn.microsoft.com/library/windows/desktop/ms691318), and [IViewObjectEx](http://msdn.microsoft.com/library/windows/desktop/ms682375) interfaces.|atlctl.h|  
|[IWorkerThreadClient Interface](../vs140/IWorkerThreadClient-Interface.md)|`IWorkerThreadClient` is the interface implemented by clients of the [CWorkerThread](../vs140/CWorkerThread-Class.md) class.|atlutil.h|  
|[_U_MENUorID](../vs140/_U_MENUorID-Class.md)|This class provides wrappers for **CreateWindow** and **CreateWindowEx**.|atlwin.h|  
|[_U_RECT](../vs140/_U_RECT-Class.md)|This argument adapter class allows either `RECT` pointers or references to be passed to a function that is implemented in terms of pointers.|atlwin.h|  
|[_U_STRINGorID](../vs140/_U_STRINGorID-Class.md)|This argument adapter class allows either resource names (`LPCTSTR`s) or resource IDs (**UINT**s) to be passed to a function without requiring the caller to convert the ID to a string using the **MAKEINTRESOURCE** macro.|atlwin.h|  
|[Win32ThreadTraits](../vs140/Win32ThreadTraits-Class.md)|This class provides the creation function for a Windows thread. Use this class if the thread will not use CRT functions.|atlbase.h|  
  
## See Also  
 [ATL COM Desktop Components](../vs140/ATL-COM-Desktop-Components.md)   
 [Functions](../vs140/ATL-Functions.md)   
 [Global Variables](../vs140/ATL-Global-Variables.md)   
 [Structures](../vs140/ATL-Structures.md)   
 [Typedefs](../vs140/ATL-Typedefs.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)