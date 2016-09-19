---
title: "emitidl"
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
ms.assetid: 85b80c56-578e-4392-ac03-8443c74ebb7d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# emitidl
Determines whether all subsequent IDL attributes will be processed and placed in the generated .idl file.  
  
## Syntax  
  
```  
  
      [ emitidl([boolean],  
   defaultimports=[boolean]  
) ] ;  
```  
  
#### Parameters  
 `boolean`  
 Possible values: **true**, **false**, **forced**, **restricted**, **push**, or **pop**.  
  
-   If **true**, any IDL category attributes encountered in a source code file will be placed in the generated .idl file. This is the default setting for **emitidl**.  
  
-   If **false**, any IDL category attributes encountered in a source code file will not be placed in the generated .idl file.  
  
-   If **restricted**, allows IDL attributes to be in the file without a [module](../vs140/module--C---.md) attribute. The compiler will not generate an .idl file.  
  
-   If **forced**, overrides a subsequent **restricted** attribute, which requires a file to have a **module** attribute if there are IDL attributes in the file.  
  
-   **push** lets you save the current **emitidl** settings to an internal **emitidl** stack, and **pop** lets you set **emitidl** to whatever value is at the top of the internal **emitidl** stack.  
  
 **defaultimports** *=*[ `boolean`] (optional)  
 -   If `boolean` is **true**, docobj.idl will be imported into the generated .idl file. Also, if an .idl file with the same name as an .h file that you `#include` into your source code is found in the same directory as the .h file, then the generated .idl file will contain an import statement for that .idl file.  
  
-   If `boolean` is **false**, docobj.idl will not be imported into the generated .idl file. You will need to explicitly import .idl files with [import](../vs140/import.md).  
  
## Remarks  
 After the **emitidl** C++ attribute is encountered in a source code file, IDL category attributes will be placed in the generated .idl file. If there is no **emitidl** attribute, IDL attributes in the source code file will be output to the generated .idl file.  
  
 It is possible to have multiple **emitidl** attributes in a source code file. If `[emitidl(false)];` is encountered in a file without a subsequent `[emitidl(true)];`, then no attributes will be processed into the generated .idl file.  
  
 Each time the compiler encounters a new file, **emitidl** is implicitly set to **true**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Anywhere|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [Compiler Attributes](../vs140/Compiler-Attributes.md)   
 [Stand-Alone Attributes](../vs140/Stand-Alone-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)