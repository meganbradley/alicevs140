---
title: "error_code::error_code"
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
ms.assetid: 3fc79827-c197-4ef9-8e09-ec8cdd521173
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# error_code::error_code
Constructs an object of type `error_code`.  
  
## Syntax  
  
```  
error_code();  
error_code(value_type _Val, const error_category& _Cat);  
template<class _Enum>  
    error_code(_Enum _Errcode,  
    typename enable_if<is_error_code_enum<_Enum>::value,  
        error_code>::type * = 0);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Val`|The error code value to store in the `error_code`.|  
|`_Cat`|The error category to store in the `error_code`.|  
|`_Errcode`|The enumeration value to store in the `error_code`.|  
  
## Remarks  
 The first constructor stores a zero error code value and a pointer to the [generic_category](../vs140/generic_category.md).  
  
 The second constructor stores `_Val` as the error code value and a pointer to [error_category](assetId:///6fe57a15-63a1-4e79-8af4-6738e43e19c8).  
  
 The third constructor stores `(value_type)_Errcode` as the error code value and a pointer to the [generic_category](../vs140/generic_category.md).  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_code Class](../vs140/error_code-Class.md)