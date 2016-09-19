---
title: "ComPtr Class"
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
ms.assetid: a6551902-6819-478a-8df7-b6f312ab1fb0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr Class
Creates a *smart pointer* type that represents the interface specified by the template parameter. ComPtr automatically maintains a reference count for the underlying interface pointer and releases the interface when the reference count goes to zero.  
  
## Syntax  
  
```  
template <  
   typename T  
>  
class ComPtr;  
  
template<  
   class U  
>  
friend class ComPtr;  
```  
  
#### Parameters  
 `T`  
 The interface that the ComPtr represents.  
  
 `U`  
 A class to which the current ComPtr is a friend. (The template that uses this parameter is protected.)  
  
## Remarks  
 ComPtr<> declares a type that represents the underlying interface pointer. Use ComPtr<> to declare a variable and then use the arrow member-access operator (`->`) to access an interface member function.  
  
 For more information about smart pointers, see the "COM Smart Pointers" subsection of the [COM Coding Practices](assetId:///76aca556-b4d6-4e67-a2a3-4439900f0c39)topic in the MSDN Library.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`InterfaceType`|A synonym for the type specified by the `T` template parameter.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[ComPtr::ComPtr Constructor](../vs140/ComPtr--ComPtr-Constructor.md)|Intializes a new instance of the ComPtr class. Overloads provide default, copy, move, and conversion constructors.|  
|[ComPtr::~ComPtr Destructor](../vs140/ComPtr--~ComPtr-Destructor.md)|Deinitializes an instance of ComPtr.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ComPtr::As Method](../vs140/ComPtr--As-Method.md)|Returns a ComPtr object that represents the interface identified by the specified template parameter.|  
|[ComPtr::AsIID Method](../vs140/ComPtr--AsIID-Method.md)|Returns a ComPtr object that represents the interface identified by the specified interface ID.|  
|[ComPtr::AsWeak Method](../vs140/ComPtr--AsWeak-Method.md)|Retrieves a weak reference to the current object.|  
|[ComPtr::Attach Method](../vs140/ComPtr--Attach-Method.md)|Associates this ComPtr with the interface type specified by the current template type parameter.|  
|[ComPtr::CopyTo Method](../vs140/ComPtr--CopyTo-Method.md)|Copies the current or specified interface associated with this ComPtr to the specified output pointer.|  
|[ComPtr::Detach Method](../vs140/ComPtr--Detach-Method.md)|Disassociates this ComPtr from the interface that it represents.|  
|[ComPtr::Get Method](../vs140/ComPtr--Get-Method.md)|Retrieves a pointer to the interface that is associated with this ComPtr.|  
|[ComPtr::GetAddressOf Method](../vs140/ComPtr--GetAddressOf-Method.md)|Retrieves the address of the [ptr_](../vs140/ComPtr--ptr_-Data-Member.md) data member, which contains a pointer to the interface represented by this ComPtr.|  
|[ComPtr::ReleaseAndGetAddressOf Method](../vs140/ComPtr--ReleaseAndGetAddressOf-Method.md)|Releases the interface associated with this ComPtr and then retrieves the address of the [ptr_](../vs140/ComPtr--ptr_-Data-Member.md) data member, which contains a pointer to the interface that was released.|  
|[ComPtr::Reset Method](../vs140/ComPtr--Reset.md)|Releases all references for the pointer to the interface that is associated with this ComPtr.|  
|[ComPtr::Swap Method](../vs140/ComPtr--Swap-Method.md)|Exchanges the interface managed by the current ComPtr with the interface managed by the specified ComPtr.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ComPtr::InternalAddRef Method](../vs140/ComPtr--InternalAddRef-Method.md)|Increments the reference count of the interface associated with this ComPtr.|  
|[ComPtr::InternalRelease Method](../vs140/ComPtr--InternalRelease-Method.md)|Performs a COM Release operation on the interface associated with this ComPtr.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[ComPtr::operator Microsoft::WRL::Details::BoolType Operator](../vs140/ComPtr--operator-Microsoft--WRL--Details--BoolType-Operator.md)|Indicates whether or not a ComPtr is managing the object lifetime of an interface.|  
|[ComPtr::operator& Operator](../vs140/ComPtr--operator--Operator.md)|Retrieves the address of the current ComPtr.|  
|[ComPtr::operator= Operator](../vs140/ComPtr--operator=-Operator.md)|Assigns a value to the current ComPtr.|  
|[ComPtr::operator-> Operator](../vs140/ComPtr--operator---Operator.md)|Retrieves a pointer to the type specified by the current template parameter.|  
|[ComPtr::operator== Operator](../vs140/ComPtr--operator==-Operator.md)|Indicates whether two ComPtr objects are equal.|  
|[ComPtr::operator!= Operator](../vs140/ComPtr--operator!=-Operator.md)|Indicates whether two ComPtr objects are not equal.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[ComPtr::ptr_ Data Member](../vs140/ComPtr--ptr_-Data-Member.md)|Contains a pointer to the interface that is associated with, and managed by this ComPtr.|  
  
## Inheritance Hierarchy  
 `ComPtr`  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)