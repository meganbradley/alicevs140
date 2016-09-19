---
title: "threading (C++)"
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
ms.assetid: 9b558cd6-fbf0-4602-aed5-31c068550ce3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# threading (C++)
Specifies the threading model for a COM object.  
  
## Syntax  
  
```  
  
      [ threading(  
   model=enumeration  
) ]  
```  
  
#### Parameters  
 ***model*** (optional)  
 One of the following threading models:  
  
-   **apartment** (apartment threading)  
  
-   **neutral** (.NET Framework components with no user interface)  
  
-   **single** (simple threading)  
  
-   **free** (free threading)  
  
-   **both** (apartment and free threading)  
  
 The default value is **apartment**.  
  
## Remarks  
 The **threading** C++ attribute does not appear in the generated .idl file but will be used in the implementation of your COM object.  
  
 In ATL projects, If the [coclass](../vs140/coclass.md) attribute is also present, the threading model specified by *model* is passed as the template parameter to the [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md) class, inserted by the **coclass** attribute.  
  
 The **threading** attribute also guards access to an [event_source](../vs140/event_source.md).  
  
## Example  
 See the [licensed](../vs140/licensed.md) example for a sample use of **threading**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`|  
|**Repeatable**|No|  
|**Required attributes**|**coclass**|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [COM Attributes](../vs140/COM-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Multithreading Support for Older Code (Visual C++)](../vs140/Multithreading-Support-for-Older-Code--Visual-C---.md)   
 [Neutral Apartments](http://msdn.microsoft.com/library/windows/desktop/ms681813)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)