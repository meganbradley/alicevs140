---
title: "Compiler Options Macros"
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
ms.assetid: a869adc6-b3de-4299-b040-9ae20b45f82c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Options Macros
These macros control specific compiler features.  
  
|||  
|-|-|  
|[_ATL_ALL_WARNINGS](../vs140/_ATL_ALL_WARNINGS.md)|A symbol which enables errors in projects converted from previous versions of ATL.|  
|[_ATL_APARTMENT_THREADED](../vs140/_ATL_APARTMENT_THREADED.md)|Define if one or more of your objects use apartment threading.|  
|[_ATL_CSTRING_EXPLICIT_CONSTRUCTORS](../vs140/_ATL_CSTRING_EXPLICIT_CONSTRUCTORS.md)|Makes certain `CString` constructors explicit, preventing any unintentional conversions.|  
|[_ATL_ENABLE_PTM_WARNING](../vs140/_ATL_ENABLE_PTM_WARNING.md)|Define this macro in order to use C++ standard compliant syntax, which generates the C4867 compiler error when a non standard syntax is used to initialize a pointer to a member function.|  
|[_ATL_FREE_THREADED](../vs140/_ATL_FREE_THREADED.md)|Define if one or more of your objects use free or neutral threading.|  
|[_ATL_MULTI_THREADED](../vs140/_ATL_MULTI_THREADED.md)|A symbol that indicates the project will have objects that are marked as Both, Free or Neutral. The macro [_ATL_FREE_THREADED](../vs140/_ATL_FREE_THREADED.md) should be used instead.|  
|[_ATL_NO_AUTOMATIC_NAMESPACE](../vs140/_ATL_NO_AUTOMATIC_NAMESPACE.md)|A symbol which prevents the default use of namespace as ATL.|  
|[_ATL_NO_COM_SUPPORT](../vs140/_ATL_NO_COM_SUPPORT.md)|A symbol which prevents COM-related code from being compiled with your project.|  
|[ATL_NO_VTABLE](../vs140/ATL_NO_VTABLE.md)|A symbol that prevents the vtable pointer from being initialized in the class's constructor and destructor.|  
|[ATL_NOINLINE](../vs140/ATL_NOINLINE.md)|A symbol that indicates a function should not be inlined.|  
|[_ATL_SINGLE_THREADED](../vs140/_ATL_SINGLE_THREADED.md)|Define if all of your objects use the single threading model.|  
  
## See Also  
 [Macros](../vs140/ATL-Macros.md)