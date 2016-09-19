---
title: "WeakRef Class"
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
ms.assetid: 572be703-c641-496c-8af5-ad6164670ba1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WeakRef Class
Represents a *weak reference* that can be used by only the Windows Runtime, not classic COM. A weak reference represents an object that might or might not be accessible.  
  
## Syntax  
  
```  
class WeakRef : public ComPtr<IWeakReference>  
```  
  
## Remarks  
 A WeakRef object maintains a *strong reference*, which is associated with an object, and can be valid or invalid. Call the As() or AsIID() method to obtain a strong reference. When the strong reference is valid, it can access the associated object. When the strong reference is invalid (`nullptr`), the associated object is inaccessible.  
  
 A WeakRef object is typically used to represent an object whose existence is controlled by an external thread or application. For example, construct a WeakRef object from a reference to a file object. While the file is open, the strong reference is valid. But if the file is closed, the strong reference becomes invalid.  
  
 Note that there is a behavior change in the [As](../vs140/WeakRef--As-Method.md), [AsIID](../vs140/WeakRef--AsIID-Method.md) and [CopyTo](../vs140/WeakRef--CopyTo-Method.md) methods in the Windows 10 SDK. Previously, after calling any of these methods, you could check the WeakRef for `nullptr` to determine if a strong reference was successfully obtained, as in the following code:  
  
```cpp  
WeakRef wr;  
strongComptrRef.AsWeak(&wr);  
  
// Now suppose that the object strongComPtrRef points to no longer exists  
// and the following code tries to get a strong ref from the weak ref:  
ComPtr<ISomeInterface> strongRef;  
HRESULT hr = wr.As(&strongRef);  
  
// This check won't work with the Windows 10 SDK version of the library.  
// Check the input pointer instead.  
if(wr == nullptr)  
{  
    wprintf(L"Couldn’t get strong ref!");  
}  
  
```  
  
 The above code does not work when using the Windows 10 SDK (or later). Instead, check the pointer that was passed in for `nullptr`.  
  
```cpp  
if (strongRef == nullptr)  
{  
    wprintf(L"Couldn't get strong ref!");  
 }  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[WeakRef::WeakRef Constructor](../vs140/WeakRef--WeakRef-Constructor.md)|Initializes a new instance of the WeakRef class.|  
|[WeakRef::~WeakRef Destructor](../vs140/WeakRef--~WeakRef-Destructor.md)|Deinitializes the current instance of the WeakRef class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[WeakRef::As Method](../vs140/WeakRef--As-Method.md)|Sets the specified ComPtr pointer parameter to represent the specified interface.|  
|[WeakRef::AsIID Method](../vs140/WeakRef--AsIID-Method.md)|Sets the specified ComPtr pointer parameter to represent the specified interface ID.|  
|[WeakRef::CopyTo Method](../vs140/WeakRef--CopyTo-Method.md)|Assigns a pointer to an interface, if available, to the specified pointer variable.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[WeakRef::operator& Operator](../vs140/WeakRef--operator--Operator.md)|Returns a ComPtrRef object that represents the current WeakRef object.|  
  
## Inheritance Hierarchy  
 `ComPtr`  
  
 `WeakRef`  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)