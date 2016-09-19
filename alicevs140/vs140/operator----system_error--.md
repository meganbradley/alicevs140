---
title: "operator&lt; (&lt;system_error&gt;)"
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
ms.assetid: 1d1ceba2-8f59-4091-bcef-c05ca2bd6919
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt; (&lt;system_error&gt;)
Tests if an object is less than the object passed in for comparison.  
  
## Syntax  
  
```  
template<class _Enum> inline bool operator<(  
    _Enum _Left,  
    typename enable_if<is_error_code_enum<_Enum>::value,  
    const error_code&>::type _Right);  
template<class _Enum> inline bool operator<(  
    typename enable_if<is_error_code_enum<_Enum>::value,  
    const error_code&>::type _Left, _Enum _Right);  
template<class _Enum> inline bool operator<(  
    _Enum _Left,  
    typename enable_if<is_error_condition_enum<_Enum>::value,  
    const error_condition&>::type _Right);  
template<class _Enum> inline bool operator<(  
    typename enable_if<is_error_condition_enum<_Enum>::value,  
    const error_condition&>::type _Left, _Enum _Right);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Left`|The object to be compared.|  
|`_Right`|The object to be compared.|  
  
## Return Value  
 **true** if the object passed in `_Left` is less than the object passed in `_Right`; Otherwise, **false**.  
  
## Remarks  
 This function tests the error order.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [<system_error>](../vs140/-system_error-.md)