---
title: "CComCoClass Class"
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
ms.assetid: 67cfefa4-8df9-47fa-ad58-2d1a1ae25762
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCoClass Class
This class provides methods for creating instances of a class, and obtaining its properties.  
  
## Syntax  
  
```  
  
template<  
      class  T,  
      const CLSID*  pclsid  
    = &CLSID_NULL>  
   class CComCoClass  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `CComCoClass`.  
  
 *pclsid*  
 A pointer to the CLSID of the object.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComCoClass::CreateInstance](../vs140/CComCoClass--CreateInstance.md)|(Static) Creates an instance of the class and queries for an interface.|  
|[CComCoClass::Error](../vs140/CComCoClass--Error.md)|(Static) Returns rich error information to the client.|  
|[CComCoClass::GetObjectCLSID](../vs140/CComCoClass--GetObjectCLSID.md)|(Static) Returns the object's class identifier.|  
|[CComCoClass::GetObjectDescription](../vs140/CComCoClass--GetObjectDescription.md)|(Static) Override to return the object's description.|  
  
## Remarks  
 `CComCoClass` provides methods for retrieving an object's CLSID, setting error information, and creating instances of the class. Any class registered in the [object map](assetId:///b57619cc-534f-4b8f-bfd4-0c12f937202f) should be derived from `CComCoClass`.  
  
 `CComCoClass` also defines the default class factory and aggregation model for your object. `CComCoClass` uses the following two macros:  
  
-   [DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md) Declares the class factory to be [CComClassFactory](../vs140/CComClassFactory-Class.md).  
  
-   [DECLARE_AGGREGATABLE](../vs140/DECLARE_AGGREGATABLE.md) Declares that your object can be aggregated.  
  
 You can override either of these defaults by specifying another macro in your class definition. For example, to use [CComClassFactory2](../vs140/CComClassFactory2-Class.md) instead of `CComClassFactory`, specify the [DECLARE_CLASSFACTORY2](../vs140/DECLARE_CLASSFACTORY2.md) macro:  
  
 [!CODE [NVC_ATL_COM#2](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#2)]  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomcoclass__createinstance"></a>  CComCoClass::CreateInstance  
 Use these `CreateInstance` functions to create an instance of a COM object and retrieve an interface pointer without using the COM API.  
  
```  
  
template <class  Q>  
   static HRESULT CreateInstance(  
      Q**  pp  
   );  
   template <class  Q>  
   static HRESULT CreateInstance(  
      IUnknown*  punkOuter,  
      Q**  pp  
   );  
  
```  
  
### Parameters  
 `Q`  
 The COM interface that should be returned via `pp`.  
  
 *punkOuter*  
 [in] The outer unknown or controlling unknown of the aggregate.  
  
 `pp`  
 [out] The address of a pointer variable that receives the requested interface pointer if creation succeeds.  
  
### Return Value  
 A standard `HRESULT` value. See [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a description of possible return values.  
  
### Remarks  
 Use the first overload of this function for typical object creation; use the second overload when you need to aggregate the object being created.  
  
 The ATL class implementing the required COM object (that is, the class used as the first template parameter to [CComCoClass](../vs140/CComCoClass-Class.md)) must be in the same project as the calling code. The creation of the COM object is carried out by the class factory registered for this ATL class.  
  
 These functions are useful for creating objects that you have prevented from being externally creatable by using the [OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO](../vs140/OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO.md) macro. They are also useful in situations where you want to avoid the COM API for reasons of efficiency.  
  
 Note that the interface `Q` must have an IID associated with it that can be retrieved using the [__uuidof](../vs140/__uuidof-Operator.md) operator.  
  
### Example  
 In the following example, `CDocument` is a wizard-generated ATL class derived from `CComCoClass` that implements the **IDocument** interface. The class is registered in the object map with the `OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO` macro so clients can't create instances of the document using [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615). `CApplication` is a CoClass that provides a method on one of its own COM interfaces to create instances of the document class. The code below shows how easy it to create instances of the document class using the `CreateInstance` member inherited from the `CComCoClass` base class.  
  
 [!CODE [NVC_ATL_COM#11](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#11)]  
  
##  <a name="ccomcoclass__error"></a>  CComCoClass::Error  
 This static function sets up the `IErrorInfo` interface to provide error information to the client.  
  
```  
  
static HRESULT WINAPI Error(  
      LPCOLESTR  lpszDesc,  
      const IID&  iid  
    = GUID_NULL,  
      HRESULT  hRes  
    = 0   
   );  
   static HRESULT WINAPI Error(  
      LPCOLESTR  lpszDesc,  
      DWORD  dwHelpID,  
      LPCOLESTR  lpszHelpFile,  
      const IID&  iid  
    = GUID_NULL,  
      HRESULT  hRes  
    = 0   
   );  
   static HRESULT WINAPI Error(  
      LPCSTR  lpszDesc,  
      const IID&  iid  
    = GUID_NULL,  
      HRESULT  hRes  
    = 0   
   );  
   static HRESULT WINAPI Error(  
      LPCSTR  lpszDesc,  
      DWORD  dwHelpID,  
      LPCSTR  lpszHelpFile,  
      const IID&  iid  
    = GUID_NULL,  
      HRESULT  hRes  
    = 0   
   );  
   static HRESULT WINAPI Error(  
      UINT  nID,  
      const IID&  iid  
    = GUID_NULL,  
      HRESULT  hRes  
    = 0,  
      HINSTANCE  hInst  
    = _AtlBaseModule.GetResourceInstance ()  
   );  
   static HRESULT Error(  
      UINT  nID,  
      DWORD  dwHelpID,  
      LPCOLESTR  lpszHelpFile,  
      const IID&  iid  
    = GUID_NULL,  
      HRESULT  hRes  
    = 0,  
      HINSTANCE  hInst  
    = _AtlBaseModule.GetResourceInstance()   
   );  
  
```  
  
### Parameters  
 `lpszDesc`  
 [in] The string describing the error. The Unicode version of `Error` specifies that `lpszDesc` is of type **LPCOLESTR**; the ANSI version specifies a type of `LPCSTR`.  
  
 `iid`  
 [in] The IID of the interface defining the error or `GUID_NULL` (the default value) if the error is defined by the operating system.  
  
 `hRes`  
 [in] The `HRESULT` you want returned to the caller. The default value is 0. For more details about `hRes`, see Remarks.  
  
 `nID`  
 [in] The resource identifier where the error description string is stored. This value should lie between 0x0200 and 0xFFFF, inclusively. In debug builds, an **ASSERT** will result if `nID` does not index a valid string. In release builds, the error description string will be set to "Unknown Error."  
  
 `dwHelpID`  
 [in] The help context identifier for the error.  
  
 `lpszHelpFile`  
 [in] The path and name of the help file describing the error.  
  
 `hInst`  
 [in] The handle to the resource. By default, this parameter is **_AtlModule::GetResourceInstance**, where **_AtlModule** is the global instance of [CAtlModule](../vs140/CAtlModule-Class.md).  
  
### Return Value  
 A standard `HRESULT` value. For details, see Remarks.  
  
### Remarks  
 To call `Error`, your object must implement the `ISupportErrorInfo Interface` interface.  
  
 If the `hRes` parameter is nonzero, then `Error` returns the value of `hRes`. If `hRes` is zero, then the first four versions of `Error` return `DISP_E_EXCEPTION`. The last two versions return the result of the macro **MAKE_HRESULT( 1, FACILITY_ITF,** `nID` **)**.  
  
##  <a name="ccomcoclass__getobjectclsid"></a>  CComCoClass::GetObjectCLSID  
 Provides a consistent way of retrieving the object's CLSID.  
  
```  
  
static const CLSID& WINAPI GetObjectCLSID( );  
  
```  
  
### Return Value  
 The object's class identifier.  
  
##  <a name="ccomcoclass__getobjectdescription"></a>  CComCoClass::GetObjectDescription  
 This static function retrieves the text description for your class object.  
  
```  
  
static LPCTSTR WINAPI GetObjectDescription( );  
  
```  
  
### Return Value  
 The class object's description.  
  
### Remarks  
 The default implementation returns **NULL**. You can override this method with the [DECLARE_OBJECT_DESCRIPTION](../vs140/DECLARE_OBJECT_DESCRIPTION.md) macro. For example:  
  
 [!CODE [NVC_ATL_COM#12](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#12)]  
  
 `GetObjectDescription` is called by **IComponentRegistrar::GetComponents**.                         **IComponentRegistrar** is an Automation interface that allows you to register and unregister individual components in a DLL. When you create a Component Registrar object with the ATL Project Wizard, the wizard will automatically implement the **IComponentRegistrar** interface. **IComponentRegistrar** is typically used by Microsoft Transaction Server.  
  
 For more information about the ATL Project Wizard, see the article [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md).  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)