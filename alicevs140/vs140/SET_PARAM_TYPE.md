---
title: "SET_PARAM_TYPE"
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
ms.assetid: 85979070-2d55-4c67-94b1-9b9058babc59
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SET_PARAM_TYPE
Specifies `COLUMN_ENTRY` macros that follow the `SET_PARAM_TYPE` macro input, output, or input/output.  
  
## Syntax  
  
```  
  
SET_PARAM_TYPE(  
type  
 )  
  
```  
  
#### Parameters  
 `type`  
 [in] The type to set for the parameter.  
  
## Remarks  
 Providers support only parameter input/output types that are supported by the underlying data source. The type is a combination of one or more **DBPARAMIO** values (see [DBBINDING Structures](https://msdn.microsoft.com/en-us/library/ms716845.aspx) in the *OLE DB Programmer's Reference*):  
  
-   **DBPARAMIO_NOTPARAM** The accessor has no parameters. Typically, you set **eParamIO** to this value in row accessors to remind the user that parameters are ignored.  
  
-   **DBPARAMIO_INPUT** An input parameter.  
  
-   **DBPARAMIO_OUTPUT** An output parameter.  
  
-   **DBPARAMIO_INPUT &#124; DBPARAMIO_OUTPUT** The parameter is both an input and an output parameter.  
  
## Example  
 [!CODE [NVC_OLEDB_Consumer#18](../CodeSnippet/VS_Snippets_Cpp/NVC_OLEDB_Consumer#18)]  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)