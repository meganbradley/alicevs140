---
title: "CAtlWinModule Class"
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
ms.assetid: 7ec844af-0f68-4a34-b0c8-9de50a025df0
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlWinModule Class
This class provides support for ATL windowing components.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CAtlWinModule : public _ATL_WIN_MODULE  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlWinModule::CAtlWinModule](../vs140/CAtlWinModule--CAtlWinModule.md)|The constructor.|  
|[CAtlWinModule::~CAtlWinModule](../vs140/CAtlWinModule--~CAtlWinModule.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlWinModule::AddCreateWndData](../vs140/CAtlWinModule--AddCreateWndData.md)|Adds a data object.|  
|[CAtlWinModule::ExtractCreateWndData](../vs140/CAtlWinModule--ExtractCreateWndData.md)|Returns a pointer to the window module data object.|  
  
## Remarks  
 This class provides support for all ATL classes which require windowing features.  
  
## Inheritance Hierarchy  
 [_ATL_WIN_MODULE](../vs140/_ATL_WIN_MODULE.md)  
  
 `CAtlWinModule`  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="catlwinmodule__addcreatewnddata"></a>  CAtlWinModule::AddCreateWndData  
 This method initializes and adds an `_AtlCreateWndData` structure.  
  
```  
  
void AddCreateWndData(  
      _AtlCreateWndData*  pData,  
      void*  pObject  
   );  
  
```  
  
### Parameters  
 `pData`  
 Pointer to the `_AtlCreateWndData` structure to be initialized and added to the current module.  
  
 `pObject`  
 Pointer to an object's **this** pointer.  
  
### Remarks  
 This method calls [AtlWinModuleAddCreateWndData](../vs140/AtlWinModuleAddCreateWndData.md) which initializes an [_AtlCreateWndData](../vs140/_AtlCreateWndData-Structure.md) structure. This structure will store the **this** pointer, used to obtain the class instance in window procedures.  
  
##  <a name="catlwinmodule__catlwinmodule"></a>  CAtlWinModule::CAtlWinModule  
 The constructor.  
  
```  
  
CAtlWinModule( );  
  
```  
  
### Remarks  
 If initialization fails, an **EXCEPTION_NONCONTINUABLE** exception is raised.  
  
##  <a name="catlwinmodule___dtorcatlwinmodule"></a>  CAtlWinModule::~CAtlWinModule  
 The destructor.  
  
```  
  
~CAtlWinModule( );  
  
```  
  
### Remarks  
 Frees all allocated resources.  
  
##  <a name="catlwinmodule__extractcreatewnddata"></a>  CAtlWinModule::ExtractCreateWndData  
 This method returns a pointer to an `_AtlCreateWndData` structure.  
  
```  
  
void* ExtractCreateWndData( );  
  
```  
  
### Return Value  
 Returns a pointer to the `_AtlCreateWndData` structure previously added with [CAtlWinModule::AddCreateWndData](../vs140/CAtlWinModule--AddCreateWndData.md), or NULL if no object is available.  
  
## See Also  
 [_ATL_WIN_MODULE](../vs140/_ATL_WIN_MODULE.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Module Classes](../vs140/ATL-Module-Classes.md)