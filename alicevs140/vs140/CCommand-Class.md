---
title: "CCommand Class"
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
ms.assetid: 0760bfc5-b9ee-4aee-8e54-31bd78714d3a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommand Class
Provides methods to set and execute a command.  
  
## Syntax  
  
```  
template <  
   class TAccessor = CNoAccessor,  
   template < typename T > class TRowset = CRowset,  
   class TMultiple = CNoMultipleResults   
>  
class CCommand :   
   public CAccessorRowset <  
      TAccessor,   
      TRowset   
   >,  
   public CCommandBase,  
   public TMultiple  
```  
  
#### Parameters  
 `TAccessor`  
 The type of accessor class (such as `CDynamicParameterAccessor`, `CDynamicStringAccessor`, or `CEnumeratorAccessor`) that you want the command to use. The default is `CNoAccessor`, which specifies that the class not support parameters or output columns.  
  
 `TRowset`  
 The type of rowset class (such as `CArrayRowset` or `CNoRowset`) that you want the command to use. The default is `CRowset`.  
  
 `TMultiple`  
 To use an OLE DB command that can return multiple results, specify [CMultipleResults](../vs140/CMultipleResults-Class.md). Otherwise, use [CNoMultipleResults](../vs140/CNoMultipleResults-Class.md). For details, see [IMultipleResults](https://msdn.microsoft.com/en-us/library/ms721289.aspx).  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[Close](../vs140/CCommand--Close.md)|Closes the current command.|  
|[GetNextResult](../vs140/CCommand--GetNextResult.md)|Fetches the next result when using multiple result sets.|  
|[Open](../vs140/CCommand--Open.md)|Executes and optionally binds the command.|  
  
### Inherited Methods  
  
|||  
|-|-|  
|[Create](../vs140/CCommand--Create.md)|Creates a new command for the specified session, then sets the command text.|  
|[CreateCommand](../vs140/CCommand--CreateCommand.md)|Creates a new command.|  
|[GetParameterInfo](../vs140/CCommand--GetParameterInfo.md)|Gets a list of the command's parameters, their names, and their types.|  
|[Prepare](../vs140/CCommand--Prepare.md)|Validates and optimizes the current command.|  
|[ReleaseCommand](../vs140/CCommand--ReleaseCommand.md)|Releases the parameter accessor if necessary, then releases the command.|  
|[SetParameterInfo](../vs140/CCommand--SetParameterInfo.md)|Specifies the native type of each command parameter.|  
|[Unprepare](../vs140/CCommand--Unprepare.md)|Discards the current command execution plan.|  
  
## Remarks  
 Use this class when you need to perform a parameter-based operation or execute a command. If you merely need to open a simple rowset, use [CTable](../vs140/CTable-Class.md) instead.  
  
 The accessor class you are using determines the method of binding parameters and data.  
  
 Note that you cannot use stored procedures with the OLE DB Provider for Jet because that provider does not support stored procedures (only constants are allowed in query strings).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)