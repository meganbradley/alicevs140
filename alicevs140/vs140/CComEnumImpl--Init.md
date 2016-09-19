---
title: "CComEnumImpl::Init"
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
ms.assetid: e179097f-53ef-4e1b-bb96-371f54f9f8d9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComEnumImpl::Init
You must call this method before passing a pointer to the enumerator interface back to any clients.  
  
## Syntax  
  
```  
  
      HRESULT Init(  
   T* begin,  
   T* end,  
   IUnknown* pUnk,  
   CComEnumFlags flags = AtlFlagNoCopy   
);  
```  
  
#### Parameters  
 *begin*  
 A pointer to the first element of the array containing the items to be enumerated.  
  
 `end`  
 A pointer to the location just beyond the last element of the array containing the items to be enumerated.  
  
 *pUnk*  
 [in] The **IUnknown** pointer of an object that must be kept alive during the lifetime of the enumerator. Pass **NULL** if no such object exists.  
  
 `flags`  
 Flags specifying whether or not the enumerator should take ownership of the array or make a copy of it. Possible values are described below.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
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
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComEnumImpl Class](../vs140/CComEnumImpl-Class.md)   
 [IEnumOnSTLImpl::Init](../vs140/IEnumOnSTLImpl--Init.md)