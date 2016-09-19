---
title: "CComEnumOnSTL Class"
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
ms.assetid: befe1a44-7a00-4f28-9a2e-cc0fa526643c
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComEnumOnSTL Class
This class defines a COM enumerator object based on an STL collection.  
  
## Syntax  
  
```  
  
template <class Base,  
      const IID*  piid,  
      class  T,  
      class  Copy,  
      class  CollType,  
      class ThreadModel = CComObjectThreadModel>  
   class ATL_NO_VTABLE CComEnumOnSTL :  
      public IEnumOnSTLImpl< Base  
   ,  piid  
   ,  T  
   ,  Copy  
   ,  CollType  
   >,  
      public CComObjectRootEx< ThreadModel >  
  
```  
  
#### Parameters  
 `Base`  
 A COM enumerator ( [IEnumXXXX](https://msdn.microsoft.com/en-us/library/ms680089.aspx)) interface.  
  
 `piid`  
 A pointer to the interface ID of the enumerator interface.  
  
 `T`  
 The type of item exposed by the enumerator interface.  
  
 `Copy`  
 A [copy policy](../vs140/ATL-Copy-Policy-Classes.md) class.  
  
 `CollType`  
 An STL container class.  
  
## Remarks  
 `CComEnumOnSTL` defines a COM enumerator object based on an STL collection. This class can be used on its own or in conjunction with [ICollectionOnSTLImpl](../vs140/ICollectionOnSTLImpl-Class.md). Typical steps for using this class are outlined below. For more information, see [ATL Collections and Enumerators](../vs140/ATL-Collections-and-Enumerators.md).  
  
## To use this class with ICollectionOnSTLImpl:  
  
-   `typedef` a specialization of this class.  
  
-   Use the `typedef` as the final template argument in a specialization of `ICollectionOnSTLImpl`.  
  
 See [ATL Collections and Enumerators](../vs140/ATL-Collections-and-Enumerators.md) for an example.  
  
## To use this class independently of ICollectionOnSTLImpl:  
  
-   `typedef` a specialization of this class.  
  
-   Use the `typedef` as the template argument in a specialization of `CComObject`.  
  
-   Create an instance of the `CComObject` specialization.  
  
-   Initialize the enumerator object by calling [IEnumOnSTLImpl::Init](../vs140/IEnumOnSTLImpl--Init.md).  
  
-   Return the enumerator interface to the client.  
  
## Inheritance Hierarchy  
 `CComObjectRootBase`  
  
 `Base`  
  
 [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md)  
  
 [IEnumOnSTLImpl](../vs140/IEnumOnSTLImpl-Class.md)  
  
 `CComEnumOnSTL`  
  
## Requirements  
 **Header:** atlcom.h  
  
## Example  
 The code shown below provides a generic function to handle the creation and initialization of an enumerator object:  
  
 [!CODE [NVC_ATL_COM#34](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#34)]  
  
 This template function can be used to implement the `_NewEnum` property of a collection interface as shown below:  
  
 [!CODE [NVC_ATL_COM#35](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#35)]  
  
 This code creates a `typedef` for `CComEnumOnSTL` that exposes a vector of `CComVariant`s by means of the **IEnumVariant** interface. The **CVariantCollection** class simply specializes **CreateSTLEnumerator** to work with enumerator objects of this type.  
  
## See Also  
 [IEnumOnSTLImpl](../vs140/IEnumOnSTLImpl-Class.md)   
 [ATLCollections Sample: Demonstrates ICollectionOnSTLImpl, CComEnumOnSTL, and Custom Copy Policy Classes](../vs140/Visual-C---Samples.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectThreadModel](../vs140/CComObjectThreadModel.md)   
 [IEnumOnSTLImpl Class](../vs140/IEnumOnSTLImpl-Class.md)