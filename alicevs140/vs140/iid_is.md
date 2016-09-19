---
title: "iid_is"
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
ms.assetid: 2f9b42a9-7130-4b08-9b1e-0d5d360e10ff
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# iid_is
Specifies the IID of the COM interface pointed to by an interface pointer.  
  
## Syntax  
  
```  
  
      [ iid_is(  
   "expression"  
) ]  
```  
  
#### Parameters  
 *expression*  
 A C language expression that specifies an IID of a COM interface pointed to by an interface pointer.  
  
## Remarks  
 The **iid_is** C++ attribute has the same functionality as the [iid_is](http://msdn.microsoft.com/library/windows/desktop/aa367044) MIDL attribute.  
  
## Example  
 The following code shows the use of **iid_is**:  
  
```  
// cpp_attr_ref_iid_is.cpp  
// compile with: /LD  
#include "wtypes.h"  
#include "unknwn.h"  
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]  
__interface IFireTabCtrl : IDispatch  
{  
   [id(1)] HRESULT CreateInstance([in] REFIID riid,[out, iid_is("riid")]   
   IUnknown ** ppvObject);  
};  
  
[module(name="ATLFIRELib")];  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Interface parameter, data member|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Parameter Attributes](../vs140/Parameter-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)