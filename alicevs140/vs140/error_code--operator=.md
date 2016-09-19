---
title: "error_code::operator="
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
ms.assetid: 49228f22-8e52-448a-9a6a-190749f47189
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_code::operator=
Assigns a new enumeration value to the [error_code](assetId:///09c6ef90-b6f8-430a-b584-e168716c7e31) object.  
  
## Syntax  
  
```  
template<class _Enum>  
    typename enable_if<is_error_code_enum<_Enum>::value,  
        error_code>::type&  
    operator=(_Enum _Errcode);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errcode`|The enumeration value to assign to the `error_code` object.|  
  
## Return Value  
 A reference to the `error_code` object that is being assigned the new enumeration value by the member function.  
  
## Remarks  
 The member operator stores `(value_type)_Errcode` as the error code value and a pointer to the [generic_category](../vs140/generic_category.md). It returns `*this`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_code Class](../vs140/error_code-Class.md)