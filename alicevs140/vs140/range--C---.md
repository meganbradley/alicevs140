---
title: "range (C++)"
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
ms.topic: language-reference
ms.assetid: f352f79e-ecb3-4cdd-9cdd-8406ef473594
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# range (C++)
Specifies a range of allowable values for arguments or fields whose values are set at run time.  
  
## Syntax  
  
```  
  
      [ range(  
   low,   
   high  
) ]  
```  
  
#### Parameters  
 *low*  
 The low range value.  
  
 *high*  
 The high range value.  
  
## Remarks  
 The **range** C++ attribute has the same functionality as the [range](http://msdn.microsoft.com/library/windows/desktop/aa367151) MIDL attribute.  
  
## Example  
  
```  
// cpp_attr_ref_range.cpp  
// compile with: /LD  
#include <unknwn.h>  
[module(name="MyLib")];  
  
[object, uuid("9E66A290-4365-11D2-A997-00C04FA37DDB")]  
__interface ICustom {  
   HRESULT Custom([in] long l, [out, retval] long *pLong);  
   HRESULT length_is1([in, range(0, 999)] long f, [in, length_is(f)] char array[10]);  
   HRESULT length_is2([in, range(-99, -1)] long f, [in, length_is("f"), size_is(10)] char *array);  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Interface method, interface parameter|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [Parameter Attributes](../vs140/Parameter-Attributes.md)   
 [Data Member Attributes](../vs140/Data-Member-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)