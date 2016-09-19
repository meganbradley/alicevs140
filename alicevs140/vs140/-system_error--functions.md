---
title: "&lt;system_error&gt; functions"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57d6f15f-f0b7-4e2f-80fe-31d3c320ee33
caps.latest.revision: 11
---
# &lt;system_error&gt; functions
||||  
|-|-|-|  
|[generic_category](#generic_category)|[make_error_code](#make_error_code)|[make_error_condition](#make_error_condition)|  
|[system_category](#system_category)|  
  
##  <a name="generic_category"></a>  generic_category  
 Represents the category for generic errors.  
  
```  
extern const error_category& generic_category();  
```  
  
### Remarks  
 The `generic_categor`y object is an implementation of [error_category](../vs140/error_category-Class.md).  
  
##  <a name="make_error_code"></a>  make_error_code  
 Creates an error code object.  
  
```  
error_code make_error_code(generic_errno _Errno);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errno`|The enumeration value to store in the error code object.|  
  
### Return Value  
 The error code object.  
  
### Remarks  
  
##  <a name="make_error_condition"></a>  make_error_condition  
 Creates an error condition object.  
  
```  
error_condition make_error_condition(generic_errno _Errno);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errno`|The enumeration value to store in the error condition object.|  
  
### Return Value  
 The error condition object.  
  
### Remarks  
  
##  <a name="system_category"></a>  system_category  
 Represents the category for errors caused by low-level system overflows.  
  
```  
extern const error_category& system_category();  
```  
  
### Remarks  
 The `system_categor`y object is an implementation of [error_category](../vs140/error_category-Class.md).  
  
## See Also  
 [&lt;system_error&gt;](../vs140/-system_error-.md)