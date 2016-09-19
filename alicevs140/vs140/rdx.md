---
title: "rdx"
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
ms.assetid: ff8e4312-c1ad-4934-bdaa-86f54409651e
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rdx
Creates a registry key or modifies an existing registry key.  
  
## Syntax  
  
```  
  
      [ rdx(   
   key,   
   valuename=NULL,   
   regtype   
) ]  
```  
  
#### Parameters  
 `key`  
 The name of the key to be created or opened.  
  
 `valuename`(optional)  
 Specifies the value field to be set. If a value field with this name does not already exist in the key, it is added.  
  
 *regtype*  
 The type of registry key being added. Can be one of the following: **text**, **dword**, **binary**, or `CString`.  
  
## Remarks  
 The **rdx** C++ attribute creates or modifies an existing registry key for a COM component. The attribute adds a BEGIN_RDX_MAP macro to the object that implements the target member. `RegistryDataExchange`, a function injected as a result of the BEGIN_RDX_MAP macro, can be used to transfer data between the registry and the data members  
  
 This attribute can be used in conjunction with the [coclass](../vs140/coclass.md), [progid](../vs140/progid.md), or [vi_progid](../vs140/vi_progid.md) attributes or other attributes that implies one of these.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class** or `struct` member|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## Example  
 The following code adds a registry key called MyValue to the system describing the CMyClass COM component.  
  
```  
// cpp_attr_ref_rdx.cpp  
// compile with: /LD /link /OPT:NOREF  
#define _ATL_ATTRIBUTES  
#include "atlbase.h"  
  
[module (name="MyLib")];  
  
class CMyClass {  
public:  
   CMyClass() {  
      strcpy_s(m_sz, "SomeValue");  
   }  
  
   [ rdx(key = "HKCR\\MyApp.MyApp.1", valuename = "MyValue", regtype = "text")]   
   char m_sz[256];  
};  
```  
  
## See Also  
 [COM Attributes](../vs140/COM-Attributes.md)   
 [registration_script](../vs140/registration_script.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)