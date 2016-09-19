---
title: "error_condition Class"
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
ms.assetid: 6690f481-97c9-4554-a0ff-851dc96b7a06
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_condition Class
Represents user-defined error codes.  
  
## Syntax  
  
```  
class error_condition;  
```  
  
## Remarks  
 An object of type `error_condition` stores an error code value and a pointer to an object that represents a [category](../vs140/error_category-Class.md) of error codes used for reported user-defined errors.  
  
### Constructors  
  
|||  
|-|-|  
|[error_condition](#error_condition__error_condition)|Constructs an object of type `error_condition`.|  
  
### Typedefs  
  
|||  
|-|-|  
|[value_type](#error_condition__value_type)|A type that represents the stored error code value.|  
  
### Member Functions  
  
|||  
|-|-|  
|[assign](#error_condition__assign)|Assigns an error code value and category to an error condition.|  
|[category](#error_condition__category)|Returns the error category.|  
|[clear](#error_condition__clear)|Clears the error code value and category.|  
|[message](#error_condition__message)|Returns the name of the error code.|  
  
### Operators  
  
|||  
|-|-|  
|[operator==](#error_condition__operator_eq_eq)|Tests for equality between `error_condition` objects.|  
|[operator!=](#error_condition__operator_neq)|Tests for inequality between `error_condition` objects.|  
|[operator<](#error_condition__operator_lt_)|Tests if the `error_condition` object is less than the `error_code` object passed in for comparison.|  
|[operator=](#error_condition__operator_eq)|Assigns a new enumeration value to the `error_condition` object.|  
|[operator bool](#error_condition__operator_bool)|Casts a variable of type `error_condition`.|  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
##  <a name="error_condition__assign"></a>  error_condition::assign  
 Assigns an error code value and category to an error condition.  
  
```  
void assign(value_type _Val, const error_category& _Cat);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Val`|The error code value to store in the `error_code`.|  
|`_Cat`|The error category to store in the `error_code`.|  
  
### Remarks  
 The member function stores `_Val` as the error code value and a pointer to `_Cat`.  
  
##  <a name="error_condition__category"></a>  error_condition::category  
 Returns the error category.  
  
```  
const error_category& category() const;  
```  
  
### Return Value  
 A reference to the stored error category  
  
### Remarks  
  
##  <a name="error_condition__clear"></a>  error_condition::clear  
 Clears the error code value and category.  
  
```  
clear();  
```  
  
### Remarks  
 The member function stores a zero error code value and a pointer to the [generic_category](../vs140/-system_error--functions.md#generic_category) object.  
  
##  <a name="error_condition__error_condition"></a>  error_condition::error_condition  
 Constructs an object of type `error_condition`.  
  
```  
error_condition();  
error_condition(value_type _Val, const error_category& _Cat);  
template<class _Enum>  
    error_condition(_Enum _Errcode,  
    typename enable_if<is_error_condition_enum<_Enum>::value,  
        error_code>::type * = 0);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Val`|The error code value to store in the `error_condition`.|  
|`_Cat`|The error category to store in the `error_condition`.|  
|`_Errcode`|The enumeration value to store in the `error_condition`.|  
  
### Remarks  
 The first constructor stores a zero error code value and a pointer to the [generic_category](../vs140/-system_error--functions.md#generic_category).  
  
 The second constructor stores `_Val` as the error code value and a pointer to [error_category](assetId:///6fe57a15-63a1-4e79-8af4-6738e43e19c8).  
  
 The third constructor stores `(value_type)_Errcode` as the error code value and a pointer to the [generic_category](../vs140/-system_error--functions.md#generic_category).  
  
##  <a name="error_condition__message"></a>  error_condition::message  
 Returns the name of the error code.  
  
```  
string message() const;  
```  
  
### Return Value  
 A `string` representing the name of the error code.  
  
### Remarks  
 This member function returns `category().message(value())`.  
  
##  <a name="error_condition__operator_eq_eq"></a>  error_condition::operator==  
 Tests for equality between `error_condition` objects.  
  
```  
bool operator==(const error_condition& _Right) const;  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The ojbect to be tested for equality.|  
  
### Return Value  
 **true** if the objects are equal; **false** if objects are not equal.  
  
### Remarks  
 The member operator returns `category() == _Right.category() && value == _Right.value()`.  
  
##  <a name="error_condition__operator_neq"></a>  error_condition::operator!=  
 Tests for inequality between `error_condition` objects.  
  
```  
bool operator!=(const error_condition& _Right) const;  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The object to be tested for inequality.|  
  
### Return Value  
 **true** if the `error_condition` object is not equal to the `error_condition` object passed in `_Right`; otherwise **false**.  
  
### Remarks  
 The member operator returns `!(*this == _Right)`.  
  
##  <a name="error_condition__operator_lt_"></a>  error_condition::operator&lt;  
 Tests if the `error_condition` object is less than the `error_code` object passed in for comparison.  
  
```  
bool operator<(const error_condition& _Right) const;  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The `error_condition` object to be compared.|  
  
### Return Value  
 **true** if the `error_condition` object is less than the `error_condition` object passed in for comparison; Otherwise, **false**.  
  
### Remarks  
 The member operator returns `category() < _Right.category() || category() == _Right.category() && value < _Right.value()`.  
  
##  <a name="error_condition__operator_eq"></a>  error_condition::operator=  
 Assigns a new enumeration value to the `error_condition` object.  
  
```  
template<class _Enum>  
    error_condition(_Enum error,  
        typename enable_if<is_error_condition_enum<_Enum>::value,  
            error_condition>::type&  
    operator=(Enum _Errcode);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errcode`|The enumeration value to assign to the `error_condition` object.|  
  
### Return Value  
 A reference to the `error_condition` object that is being assigned the new enumeration value by the member function.  
  
### Remarks  
 The member operator stores `(value_type)error` as the error code value and a pointer to the [generic_category](../vs140/-system_error--functions.md#generic_category). It returns `*this`.  
  
##  <a name="error_condition__operator_bool"></a>  error_condition::operator bool  
 Casts a variable of type `error_condition`.  
  
```  
explicit operator bool() const;  
```  
  
### Return Value  
 The Boolean value of the `error_condition` object.  
  
### Remarks  
 The operator returns a value convertible to `true` only if [value](#error_condition__value) is not equal to zero. The return type is convertible only to `bool`, not to `void *` or other known scalar types.  
  
##  <a name="error_condition__value"></a>  error_condition::value  
 Returns the stored error code value.  
  
```  
value_type value() const;  
```  
  
### Return Value  
 The stored error code value of type [value_type](#error_condition__value_type).  
  
### Remarks  
  
##  <a name="error_condition__value_type"></a>  error_condition::value_type  
 A type that represents the stored error code value.  
  
```  
typedef int value_type;  
```  
  
### Remarks  
 The type definition is a synonym for `int`.  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)   
 [<system_error>](../vs140/-system_error-.md)