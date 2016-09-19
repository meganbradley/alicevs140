---
title: "CAtlAutoThreadModule Class"
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
ms.assetid: 3be834aa-55ef-403e-94ae-41979691b15f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlAutoThreadModule Class
This class implements a thread-pooled, apartment-model COM server.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CAtlAutoThreadModule :  
   public CAtlAutoThreadModuleT< CAtlAutoThreadModule >  
  
```  
  
## Remarks  
 `CAtlAutoThreadModule` derives from [CAtlAutoThreadModuleT](../vs140/CAtlAutoThreadModuleT-Class.md) and implements a thread-pooled, apartment-model COM server. `CAtlAutoThreadModule` uses [CComApartment](../vs140/CComApartment-Class.md) to manage an apartment for each thread in the module.  
  
 You must use the [DECLARE_CLASSFACTORY_AUTO_THREAD](../vs140/DECLARE_CLASSFACTORY_AUTO_THREAD.md) macro in your object's class definition to specify [CComClassFactoryAutoThread](../vs140/CComClassFactoryAutoThread-Class.md) as the class factory. You should then add a single instance of a class derived from `CAtlAutoThreadModuleT` such as `CAtlAutoThreadModule`. For example:  
  
 `CAtlAutoThreadModule _AtlAutoModule; // name is immaterial.`  
  
> [!NOTE]
>  This class replaces the obsolete [CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md) class.  
  
## Inheritance Hierarchy  
 `IAtlAutoThreadModule`  
  
 [CAtlAutoThreadModuleT](../vs140/CAtlAutoThreadModuleT-Class.md)  
  
 `CAtlAutoThreadModule`  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlAutoThreadModuleT Class](../vs140/CAtlAutoThreadModuleT-Class.md)   
 [IAtlAutoThreadModule Class](../vs140/IAtlAutoThreadModule-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Module Classes](../vs140/ATL-Module-Classes.md)