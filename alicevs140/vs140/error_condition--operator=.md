---
title: "error_condition::operator="
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
ms.topic: article
ms.assetid: 1019f38b-da36-4e70-afde-3ad70fbafc20
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_condition::operator=
Assigns a new enumeration value to the `error_condition` object.  
  
## Syntax  
  
```  
template<class _Enum>  
    error_condition(_Enum error,  
        typename enable_if<is_error_condition_enum<_Enum>::value,  
            error_condition>::type&  
    operator=(Enum _Errcode);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errcode`|The enumeration value to assign to the `error_condition` object.|  
  
## Return Value  
 A reference to the `error_condition` object that is being assigned the new enumeration value by the member function.  
  
## Remarks  
 The member operator stores `(value_type)error` as the error code value and a pointer to the [generic_category](../vs140/generic_category.md). It returns `*this`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_condition Class](../vs140/error_condition-Class.md)