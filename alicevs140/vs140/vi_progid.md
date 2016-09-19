---
title: "vi_progid"
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
ms.assetid: a52449be-b93e-4111-b883-44bb8da53261
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vi_progid
Specifies a version-independent form of the ProgID.  
  
## Syntax  
  
```  
  
      [ vi_progid(  
   name  
) ];  
```  
  
#### Parameters  
 *name*  
 The version-independent ProgID representing the object.  
  
 ProgIDs present a human-readable version of the class identifier (CLSID) used to identify COM/ActiveX objects.  
  
## Remarks  
 The **vi_progid** C++ attribute lets you specify a version-independent ProgID for a COM object. A ProgID has the form *name1*.*name2*.*version*. A version-independent ProgID does not have a *version*. It is possible to specify both the **progid** and the **vi_progid** attributes on a coclass. If you do not specify **vi_progid**, the version-independent ProgID is the value specified by the [progid](../vs140/progid.md) attribute.  
  
 **vi_progid** implies the **coclass** attribute, that is, if you specify **vi_progid**, it is the same thing as specifying the **coclass** and **vi_progid** attributes.  
  
 The **vi_progid** attribute causes a class to be automatically registered under the specified name. The generated .idl file will not display the ProgID value.  
  
 In ATL projects, If the [coclass](../vs140/coclass.md) attribute is also present, the specified ProgID is used by the **GetVersionIndependentProgID** function (inserted by the **coclass** attribute).  
  
## Example  
 See the [coclass](../vs140/coclass.md) example for a sample use of **vi_progid**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [ProgID Key](http://msdn.microsoft.com/library/windows/desktop/dd542719)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)