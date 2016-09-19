---
title: "CComEnumImpl Class"
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
ms.assetid: cc0d8e76-e608-46db-87cd-4c7161fe32d2
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComEnumImpl Class
This class provides the implementation for a COM enumerator interface where the items being enumerated are stored in an array.  
  
## Syntax  
  
```  
  
template <class Base,  
      const IID*  piid,  
      class  T,  
      class  Copy>  
   class ATL_NO_VTABLE CComEnumImpl :   
      public  Base  
  
```  
  
#### Parameters  
 `Base`  
 A COM enumerator ( [IEnumXXXX](https://msdn.microsoft.com/en-us/library/ms680089.aspx)) interface.  
  
 `piid`  
 A pointer to the interface ID of the enumerator interface.  
  
 `T`  
 The type of item exposed by the enumerator interface.  
  
 `Copy`  
 A homogeneous [copy policy class](../vs140/ATL-Copy-Policy-Classes.md).  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComEnumImpl::CComEnumImpl](../vs140/CComEnumImpl--CComEnumImpl.md)|The constructor.|  
|[CComEnumImpl::~CComEnumImpl](../vs140/CComEnumImpl--~CComEnumImpl.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComEnumImpl::Clone](../vs140/CComEnumImpl--Clone.md)|The implementation of [IEnumXXXX::Clone](https://msdn.microsoft.com/en-us/library/ms690336.aspx).|  
|[CComEnumImpl::Init](../vs140/CComEnumImpl--Init.md)|Initializes the enumerator.|  
|[CComEnumImpl::Next](../vs140/CComEnumImpl--Next.md)|The implementation of [IEnumXXXX::Next](https://msdn.microsoft.com/en-us/library/ms695273.aspx).|  
|[CComEnumImpl::Reset](../vs140/CComEnumImpl--Reset.md)|The implementation of [IEnumXXXX::Reset](https://msdn.microsoft.com/en-us/library/ms693414.aspx).|  
|[CComEnumImpl::Skip](../vs140/CComEnumImpl--Skip.md)|The implementation of [IEnumXXXX::Skip](https://msdn.microsoft.com/en-us/library/ms690392.aspx).|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComEnumImpl::m_begin](../vs140/CComEnumImpl--m_begin.md)|A pointer to the first item in the array.|  
|[CComEnumImpl::m_dwFlags](../vs140/CComEnumImpl--m_dwFlags.md)|Copy flags passed through `Init`.|  
|[CComEnumImpl::m_end](../vs140/CComEnumImpl--m_end.md)|A pointer to the location just beyond the last item in the array.|  
|[CComEnumImpl::m_iter](../vs140/CComEnumImpl--m_iter.md)|A pointer to the current item in the array.|  
|[CComEnumImpl::m_spUnk](../vs140/CComEnumImpl--m_spUnk.md)|The **IUnknown** pointer of the object supplying the collection being enumerated.|  
  
## Remarks  
 `CComEnumImpl` provides the implementation for a COM enumerator interface where the items being enumerated are stored in an array. This class is analogous to the `IEnumOnSTLImpl` class, which provides an implementation of an enumerator interface based on an STL container.  
  
> [!NOTE]
>  For details on further differences between `CComEnumImpl` and `IEnumOnSTLImpl`, see [CComEnumImpl::Init](../vs140/CComEnumImpl--Init.md).  
  
 Typically, you will *not* need to create your own enumerator class by deriving from this interface implementation. If you want to use an ATL-supplied enumerator based on an array, it is more common to create an instance of [CComEnum](../vs140/CComEnum-Class.md).  
  
 However, if you do need to provide a custom enumerator (for example, one that exposes interfaces in addition to the enumerator interface), you can derive from this class. In this situation, it is likely that you'll need to override the [CComEnumImpl::Clone](../vs140/CComEnumImpl--Clone.md) method to provide your own implementation.  
  
 For more information, see [ATL Collections and Enumerators](../vs140/ATL-Collections-and-Enumerators.md).  
  
## Inheritance Hierarchy  
 `Base`  
  
 `CComEnumImpl`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomenumimpl__ccomenumimpl"></a>  CComEnumImpl::CComEnumImpl  
 The constructor.  
  
```  
  
CComEnumImpl( );  
  
```  
  
##  <a name="ccomenumimpl___dtorccomenumimpl"></a>  CComEnumImpl::~CComEnumImpl  
 The destructor.  
  
```  
  
~CComEnumImpl( );  
  
```  
  
##  <a name="ccomenumimpl__init"></a>  CComEnumImpl::Init  
 You must call this method before passing a pointer to the enumerator interface back to any clients.  
  
```  
  
HRESULT Init(  
      T*  begin,  
      T*  end,  
      IUnknown*  pUnk,  
      CComEnumFlags  flags  
    = AtlFlagNoCopy   
   );  
  
```  
  
### Parameters  
 *begin*  
 A pointer to the first element of the array containing the items to be enumerated.  
  
 `end`  
 A pointer to the location just beyond the last element of the array containing the items to be enumerated.  
  
 *pUnk*  
 [in] The **IUnknown** pointer of an object that must be kept alive during the lifetime of the enumerator. Pass **NULL** if no such object exists.  
  
 `flags`  
 Flags specifying whether or not the enumerator should take ownership of the array or make a copy of it. Possible values are described below.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 Only call this method once — initialize the enumerator, use it, then throw it away.  
  
 If you pass pointers to items in an array held in another object (and you don't ask the enumerator to copy the data), you can use the *pUnk* parameter to ensure that the object and the array it holds are available for as long as the enumerator needs them. The enumerator simply holds a COM reference on the object to keep it alive. The COM reference is automatically released when the enumerator is destroyed.  
  
 The `flags` parameter allows you to specify how the enumerator should treat the array elements passed to it. `flags` can take one of the values from the **CComEnumFlags** enumeration shown below:  
  
 `enum CComEnumFlags`  
  
 `{`  
  
 `AtlFlagNoCopy = 0,`  
  
 `AtlFlagTakeOwnership = 2, // BitOwn`  
  
 `AtlFlagCopy = 3           // BitOwn | BitCopy`  
  
 `};`  
  
 **AtlFlagNoCopy** means that the array's lifetime is not controlled by the enumerator. In this case, either the array will be static or the object identified by *pUnk* will be responsible for freeing the array when it's no longer needed.  
  
 **AtlFlagTakeOwnership** means that the destruction of the array is to be controlled by the enumerator. In this case, the array must have been dynamically allocated using **new**. The enumerator will delete the array in its destructor. Typically, you would pass **NULL** for *pUnk*, although you can still pass a valid pointer if you need to be notified of the destruction of the enumerator for some reason.  
  
 **AtlFlagCopy** means that a new array is to be created by copying the array passed to `Init`. The new array's lifetime is to be controlled by the enumerator. The enumerator will delete the array in its destructor. Typically, you would pass **NULL** for *pUnk*, although you can still pass a valid pointer if you need to be notified of the destruction of the enumerator for some reason.  
  
> [!NOTE]
>  The prototype of this method specifies the array elements as being of type **T**, where **T** was defined as a template parameter to the class. This is the same type that is exposed by means of the COM interface method [CComEnumImpl::Next](../vs140/CComEnumImpl--Next.md). The implication of this is that, unlike [IEnumOnSTLImpl](../vs140/IEnumOnSTLImpl-Class.md), this class does not support different storage and exposed data types. The data type of elements in the array must be the same as the data type exposed by means of the COM interface.  
  
##  <a name="ccomenumimpl__clone"></a>  CComEnumImpl::Clone  
 This method provides the implementation of the [IEnumXXXX::Clone](https://msdn.microsoft.com/en-us/library/ms690336.aspx) method by creating an object of type `CComEnum`, initializing it with the same array and iterator used by the current object, and returning the interface on the newly created object.  
  
```  
  
STDMETHOD(Clone)(  
      Base**  ppEnum   
   );  
  
```  
  
### Parameters  
 `ppEnum`  
 [out] The enumerator interface on a newly created object cloned from the current enumerator.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 Note that cloned enumerators never make their own copy (or take ownership) of the data used by the original enumerator. If necessary, cloned enumerators will keep the original enumerator alive (using a COM reference) to ensure that the data is available for as long as they need it.  
  
##  <a name="ccomenumimpl__m_spunk"></a>  CComEnumImpl::m_spUnk  
 This smart pointer maintains a reference on the object passed to [CComEnumImpl::Init](../vs140/CComEnumImpl--Init.md), ensuring that it remains alive during the lifetime of the enumerator.  
  
```  
  
CComPtr<IUnknown> m_spUnk;  
  
```  
  
##  <a name="ccomenumimpl__m_begin"></a>  CComEnumImpl::m_begin  
 A pointer to the location just beyond the last element of the array containing the items to be enumerated.  
  
```  
  
T* m_begin;  
  
```  
  
##  <a name="ccomenumimpl__m_end"></a>  CComEnumImpl::m_end  
 A pointer to the first element of the array containing the items to be enumerated.  
  
```  
  
T* m_end;  
  
```  
  
##  <a name="ccomenumimpl__m_iter"></a>  CComEnumImpl::m_iter  
 A pointer to the current element of the array containing the items to be enumerated.  
  
```  
  
T* m_iter;  
  
```  
  
##  <a name="ccomenumimpl__m_dwflags"></a>  CComEnumImpl::m_dwFlags  
 The flags passed to [CComEnumImpl::Init](../vs140/CComEnumImpl--Init.md).  
  
```  
  
DWORD m_dwFlags;  
  
```  
  
##  <a name="ccomenumimpl__next"></a>  CComEnumImpl::Next  
 This method provides the implementation of the [IEnumXXXX::Next](https://msdn.microsoft.com/en-us/library/ms695273.aspx) method.  
  
```  
  
STDMETHOD(Next)(  
      ULONG  celt,  
      T*  rgelt,  
      ULONG*  pceltFetched   
   );  
  
```  
  
### Parameters  
 `celt`  
 [in] The number of elements requested.  
  
 `rgelt`  
 [out] The array to be filled with the elements.  
  
 `pceltFetched`  
 [out] The number of elements actually returned in `rgelt`. This can be less than `celt` if fewer than `celt` elements remained in the list.  
  
### Return Value  
 A standard `HRESULT` value.  
  
##  <a name="ccomenumimpl__reset"></a>  CComEnumImpl::Reset  
 This method provides the implementation of the [IEnumXXXX::Reset](https://msdn.microsoft.com/en-us/library/ms693414.aspx) method.  
  
```  
  
STDMETHOD(Reset)(  
      void   
   );  
  
```  
  
### Return Value  
 A standard `HRESULT` value.  
  
##  <a name="ccomenumimpl__skip"></a>  CComEnumImpl::Skip  
 This method provides the implementation of the [IEnumXXXX::Skip](https://msdn.microsoft.com/en-us/library/ms690392.aspx) method.  
  
```  
  
STDMETHOD(Skip)(  
      ULONG  celt   
   );  
  
```  
  
### Parameters  
 `celt`  
 [in] The number of elements to skip.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 Returns E_INVALIDARG if `celt` is zero, returns S_FALSE if less than `celt` elements are returned, returns S_OK otherwise.  
  
## See Also  
 [IEnumOnSTLImpl Class](../vs140/IEnumOnSTLImpl-Class.md)   
 [CComEnum Class](../vs140/CComEnum-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)