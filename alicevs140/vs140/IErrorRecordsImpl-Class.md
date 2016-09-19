---
title: "IErrorRecordsImpl Class"
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
ms.assetid: dea8e938-c5d8-45ab-86de-eb8fbf534ffb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IErrorRecordsImpl Class
Implements the OLE DB [IErrorRecords](https://msdn.microsoft.com/en-us/library/ms718112.aspx) interface, adding records to and retrieving records from a data member ([m_rgErrors](../vs140/IErrorRecordsImpl--m_rgErrors.md)) of type **CAtlArray<**`RecordClass`**>**.  
  
## Syntax  
  
```  
template <  
   class T,   
   class RecordClass = ATLERRORINFO  
>  
class IErrorRecordsImpl : public IErrorRecords  
```  
  
#### Parameters  
 `T`  
 A class derived from `IErrorRecordsImpl`.  
  
 `RecordClass`  
 A class that represents an OLE DB error object.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[GetErrorDescriptionString](../vs140/IErrorRecordsImpl--GetErrorDescriptionString.md)|Gets the error description string from an error record.|  
|[GetErrorGUID](../vs140/IErrorRecordsImpl--GetErrorGUID.md)|Gets the error GUID from an error record.|  
|[GetErrorHelpContext](../vs140/IErrorRecordsImpl--GetErrorHelpContext.md)|Gets the help context ID from an error record.|  
|[GetErrorHelpFile](../vs140/IErrorRecordsImpl--GetErrorHelpFile.md)|Gets the full pathname of the help file from an error record.|  
|[GetErrorSource](../vs140/IErrorRecordsImpl--GetErrorSource.md)|Gets the error source code from an error record.|  
  
### Interface Methods  
  
|||  
|-|-|  
|[AddErrorRecord](../vs140/IErrorRecordsImpl--AddErrorRecord.md)|Adds a record to the OLE DB error object.|  
|[GetBasicErrorInfo](../vs140/CDBErrorInfo--GetBasicErrorInfo.md)|Returns basic information about the error, such as the return code and provider-specific error number.|  
|[GetCustomErrorObject](../vs140/CDBErrorInfo--GetCustomErrorObject.md)|Returns a pointer to an interface on a custom error object.|  
|[GetErrorInfo](../vs140/CDBErrorInfo--GetErrorInfo.md)|Returns an [IErrorInfo](https://msdn.microsoft.com/en-us/library/ms718112.aspx) interface pointer on the specified record.|  
|[GetErrorParameters](../vs140/CDBErrorInfo--GetErrorParameters.md)|Returns the error parameters.|  
|[GetRecordCount](../vs140/CDaoRecordset--GetRecordCount.md)|Returns the number of records in the OLE DB record object.|  
  
### Data Members  
  
|||  
|-|-|  
|[m_rgErrors](../vs140/IErrorRecordsImpl--m_rgErrors.md)|An array of error records.|  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)