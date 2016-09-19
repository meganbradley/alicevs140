---
title: "CRuntimeClass Structure"
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
ms.assetid: de62b6ef-90d4-420f-8c70-f58b36976a2b
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRuntimeClass Structure
Each class derived from `CObject` is associated with a `CRuntimeClass` structure that you can use to obtain information about an object or its base class at run time.  
  
## Syntax  
  
```  
struct CRuntimeClass  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CRuntimeClass::CreateObject](#cruntimeclass__createobject)|Creates an object during run time.|  
|[CRuntimeClass::FromName](#cruntimeclass__fromname)|Creates an object during run time using the familiar class name.|  
|[CRuntimeClass::IsDerivedFrom](#cruntimeclass__isderivedfrom)|Determines if the class is derived from the specified class.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CRuntimeClass::m_lpszClassName](#cruntimeclass__m_lpszclassname)|The name of the class.|  
|[CRuntimeClass::m_nObjectSize](#cruntimeclass__m_nobjectsize)|The size of the object in bytes.|  
|[CRuntimeClass::m_pBaseClass](#cruntimeclass__m_pbaseclass)|A pointer to the `CRuntimeClass` structure of the base class.|  
|[CRuntimeClass::m_pfnCreateObject](#cruntimeclass__m_pfncreateobject)|A pointer to the function that dynamically creates the object.|  
|[CRuntimeClass::m_pfnGetBaseClass](#cruntimeclass__m_pfngetbaseclass)|Returns the `CRuntimeClass` structure (only available when dynamically linked).|  
|[CRuntimeClass::m_wSchema](#cruntimeclass__m_wschema)|The schema number of the class.|  
  
## Remarks  
 `CRuntimeClass` is a structure and therefore does not have a base class.  
  
 The ability to determine the class of an object at run time is useful when extra type checking of function arguments is needed, or when you must write special-purpose code based on the class of an object. Run-time class information is not supported directly by the C++ language.  
  
 `CRuntimeClass` provides information on the related C++ object, such as a pointer to the `CRuntimeClass` of the base class and the ASCII class name of the related class. This structure also implements various functions that can be used to dynamically create objects, specifying the type of object by using a familiar name, and determining if the related class is derived from a specific class.  
  
 For more information on using `CRuntimeClass`, see the article [Accessing Run-Time Class Information](../vs140/Accessing-Run-Time-Class-Information.md).  
  
## Inheritance Hierarchy  
 `CRuntimeClass`  
  
## Requirements  
 **Header:** afx.h  
  
##  <a name="cruntimeclass__createobject"></a>  CRuntimeClass::CreateObject  
 Call this function to dynamically create the specified class during run time.  
  
```  
CObject* CreateObject( ); static CObject* PASCAL CreateObject(    LPCSTR lpszClassName ); static CObject* PASCAL CreateObject(    LPCWSTR lpszClassName );  
  
```  
  
### Parameters  
 `lpszClassName`  
 The familiar name of the class to be created.  
  
### Return Value  
 A pointer to the newly created object, or **NULL** if the class name is not found or there is insufficient memory to create the object.  
  
### Remarks  
 Classes derived from `CObject` can support dynamic creation, which is the ability to create an object of a specified class at run time. Document, view, and frame classes, for example, should support dynamic creation. For more information on dynamic creation and the `CreateObject` member, see [CObject Class](../vs140/Using-CObject.md) and [CObject Class: Specifying Levels of Functionality](../vs140/Specifying-Levels-of-Functionality.md).  
  
### Example  
  See the example for [IsDerivedFrom](#cruntimeclass__isderivedfrom).  
  
##  <a name="cruntimeclass__fromname"></a>  CRuntimeClass::FromName  
 Call this function to retrieve the `CRuntimeClass` structure associated with the familiar name.  
  
```  
static CRuntimeClass* PASCAL FromName(    LPCSTR lpszClassName ); static CRuntimeClass* PASCAL FromName(    LPCWSTR lpszClassName );  
  
```  
  
### Parameters  
 `lpszClassName`  
 The familiar name of a class derived from `CObject`.  
  
### Return Value  
 A pointer to a `CRuntimeClass` object, corresponding to the name as passed in `lpszClassName`. The function returns **NULL** if no matching class name was found.  
  
### Example  
 [!CODE [NVC_MFCCObjectSample#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#17)]  
  
##  <a name="cruntimeclass__isderivedfrom"></a>  CRuntimeClass::IsDerivedFrom  
 Call this function to determine if the calling class is derived from the class specified in the                 *pBaseClass* parameter.  
  
```  
BOOL IsDerivedFrom(    const CRuntimeClass*  pBaseClass  ) const;  
  
```  
  
### Parameters  
 *pBaseClass*  
 The familiar name of a class derived from `CObject`.  
  
### Return Value  
 **TRUE** if the class calling `IsDerivedFrom` is derived from the base class whose `CRuntimeClass` structure is given as a parameter; otherwise **FALSE**.  
  
### Remarks  
 The relationship is determined by "walking" from the member's class up the chain of derived classes all the way to the top. This function only returns **FALSE** if no match is found for the base class.  
  
> [!NOTE]
>  To use the `CRuntimeClass` structure, you must include the `IMPLEMENT_DYNAMIC`, `IMPLEMENT_DYNCREATE`, or `IMPLEMENT_SERIAL` macro in the implementation of the class for which you want to retrieve run-time object information.  
  
 For more information on using `CRuntimeClass`, see the article [CObject Class: Accessing Run-Time Class Information](../vs140/Accessing-Run-Time-Class-Information.md).  
  
### Example  
 [!CODE [NVC_MFCCObjectSample#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#18)]  
  
##  <a name="cruntimeclass__m_lpszclassname"></a>  CRuntimeClass::m_lpszClassName  
 A null-terminated string containing the ASCII class name.  
  
### Remarks  
 This name can be used to create an instance of the class using the `FromName` member function.  
  
### Example  
  See the example for [IsDerivedFrom](#cruntimeclass__isderivedfrom).  
  
##  <a name="cruntimeclass__m_nobjectsize"></a>  CRuntimeClass::m_nObjectSize  
 The size of the object, in bytes.  
  
### Remarks  
 If the object has data members that point to allocated memory, the size of that memory is not included.  
  
### Example  
  See the example for [IsDerivedFrom](#cruntimeclass__isderivedfrom).  
  
##  <a name="cruntimeclass__m_pbaseclass"></a>  CRuntimeClass::m_pBaseClass  
 If your application statically links to MFC, this data member contains a pointer to the `CRuntimeClass` structure of the base class.  
  
### Remarks  
 If your application dynamically links to the MFC library, see [m_pfnGetBaseClass](#cruntimeclass__m_pfngetbaseclass).  
  
### Example  
  See the example for [IsDerivedFrom](#cruntimeclass__isderivedfrom).  
  
##  <a name="cruntimeclass__m_pfncreateobject"></a>  CRuntimeClass::m_pfnCreateObject  
 A function pointer to the default constructor that creates an object of your class.  
  
### Remarks  
 This pointer is only valid if the class supports dynamic creation; otherwise, the function returns **NULL**.  
  
##  <a name="cruntimeclass__m_pfngetbaseclass"></a>  CRuntimeClass::m_pfnGetBaseClass  
 If your application uses the MFC library as a shared DLL, this data member points to a function that returns the `CRuntimeClass` structure of the base class.  
  
### Remarks  
 If your application statically links to the MFC library, see [m_pBaseClass](#cruntimeclass__m_pbaseclass).  
  
### Example  
  See the example for [IsDerivedFrom](#cruntimeclass__isderivedfrom).  
  
##  <a name="cruntimeclass__m_wschema"></a>  CRuntimeClass::m_wSchema  
 The schema number ( -1 for nonserializable classes).  
  
### Remarks  
 For more information on schema numbers, see the [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md) macro.  
  
### Example  
  See the example for [IsDerivedFrom](#cruntimeclass__isderivedfrom).  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::GetRuntimeClass](../vs140/CObject-Class.md#cobject__getruntimeclass)   
 [CObject::IsKindOf](../vs140/CObject-Class.md#cobject__iskindof)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)   
 [IMPLEMENT_DYNAMIC](../vs140/IMPLEMENT_DYNAMIC.md)   
 [IMPLEMENT_DYNCREATE](../vs140/IMPLEMENT_DYNCREATE.md)   
 [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md)