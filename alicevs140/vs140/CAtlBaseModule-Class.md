---
title: "CAtlBaseModule Class"
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
ms.assetid: 55ade80c-9b0c-4c51-933e-2158436c1096
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlBaseModule Class
This class is instantiated in every ATL project.  
  
## Syntax  
  
```  
  
class CAtlBaseModule :  
      public _ATL_BASE_MODULE  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlBaseModule::CAtlBaseModule](../vs140/CAtlBaseModule--CAtlBaseModule.md)|The constructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlBaseModule::AddResourceInstance](../vs140/CAtlBaseModule--AddResourceInstance.md)|Adds a resource instance to the list of stored handles.|  
|[CAtlBaseModule::GetHInstanceAt](../vs140/CAtlBaseModule--GetHInstanceAt.md)|Returns a handle to a specified resource instance.|  
|[CAtlBaseModule::GetModuleInstance](../vs140/CAtlBaseModule--GetModuleInstance.md)|Returns the module instance from a `CAtlBaseModule` object.|  
|[CAtlBaseModule::GetResourceInstance](../vs140/CAtlBaseModule--GetResourceInstance.md)|Returns the resource instance from a `CAtlBaseModule` object.|  
|[CAtlBaseModule::RemoveResourceInstance](../vs140/CAtlBaseModule--RemoveResourceInstance.md)|Removes a resource instance from the list of stored handles.|  
|[CAtlBaseModule::SetResourceInstance](../vs140/CAtlBaseModule--SetResourceInstance.md)|Sets the resource instance of a `CAtlBaseModule` object.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlBaseModule::m_bInitFailed](../vs140/CAtlBaseModule--m_bInitFailed.md)|A variable that indicates if the module initialization has failed.|  
  
## Remarks  
 An instance of `CAtlBaseModule` named _AtlBaseModule is present in every ATL project, containing a handle to the module instance, a handle to the module containing resources (which by default, are one and the same), and an array of handles to modules providing primary resources. `CAtlBaseModule` can be safely accessed from multiple threads.  
  
 This class replaces the obsolete [CComModule](../vs140/CComModule-Class.md) class used in earlier versions of ATL.  
  
## Inheritance Hierarchy  
 [_ATL_BASE_MODULE](../vs140/_ATL_BASE_MODULE.md)  
  
 `CAtlBaseModule`  
  
## Requirements  
 **Header:** atlcore.h  
  
##  <a name="catlbasemodule__addresourceinstance"></a>  CAtlBaseModule::AddResourceInstance  
 Adds a resource instance to the list of stored handles.  
  
```  
  
bool AddResourceInstance(  
      HINSTANCE  hInst  
   ) throw( );  
  
```  
  
### Parameters  
 `hInst`  
 The resource instance to add.  
  
### Return Value  
 Returns true if the resource was successfully added, false otherwise.  
  
##  <a name="catlbasemodule__catlbasemodule"></a>  CAtlBaseModule::CAtlBaseModule  
 The constructor.  
  
```  
  
CAtlBaseModule( ) throw( );  
  
```  
  
### Remarks  
 Creates the `CAtlBaseModule`.  
  
##  <a name="catlbasemodule__gethinstanceat"></a>  CAtlBaseModule::GetHInstanceAt  
 Returns a handle to a specified resource instance.  
  
```  
  
HINSTANCE GetHInstanceAt(  
      int  i  
   ) throw( );  
  
```  
  
### Parameters  
 *i*  
 The number of the resource instance.  
  
### Return Value  
 Returns the handle to the resource instance, or NULL if no corresponding resource instance exists.  
  
##  <a name="catlbasemodule__getmoduleinstance"></a>  CAtlBaseModule::GetModuleInstance  
 Returns the module instance from a `CAtlBaseModule` object.  
  
```  
  
HINSTANCE GetModuleInstance( ) throw( );  
  
```  
  
### Return Value  
 Returns the module instance.  
  
##  <a name="catlbasemodule__getresourceinstance"></a>  CAtlBaseModule::GetResourceInstance  
 Returns the resource instance.  
  
```  
  
HINSTANCE GetResourceInstance( ) throw( );  
  
```  
  
### Return Value  
 Returns the resource instance.  
  
##  <a name="catlbasemodule__m_binitfailed"></a>  CAtlBaseModule::m_bInitFailed  
 A variable that indicates if the module initialization has failed.  
  
```  
  
static bool m_bInitFailed;  
  
```  
  
### Remarks  
 True if the module initialized, false if it failed to initialize.  
  
##  <a name="catlbasemodule__removeresourceinstance"></a>  CAtlBaseModule::RemoveResourceInstance  
 Removes a resource instance from the list of stored handles.  
  
```  
  
bool RemoveResourceInstance(  
      HINSTANCE  hInst  
   ) throw( );  
  
```  
  
### Parameters  
 `hInst`  
 The resource instance to remove.  
  
### Return Value  
 Returns true if the resource was successfully removed, false otherwise.  
  
##  <a name="catlbasemodule__setresourceinstance"></a>  CAtlBaseModule::SetResourceInstance  
 Sets the resource instance of a `CAtlBaseModule` object.  
  
```  
  
HINSTANCE SetResourceInstance(  
      HINSTANCE  hInst  
   ) throw( );  
  
```  
  
### Parameters  
 `hInst`  
 The new resource instance.  
  
### Return Value  
 Returns the updated resource instance.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Module Classes](../vs140/ATL-Module-Classes.md)