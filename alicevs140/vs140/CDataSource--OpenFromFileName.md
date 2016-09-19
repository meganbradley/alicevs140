---
title: "CDataSource::OpenFromFileName"
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
ms.assetid: c4226de6-59da-4368-9c15-c5afab86f68b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataSource::OpenFromFileName
Opens a data source from a file specified by the user-supplied file name.  
  
## Syntax  
  
```  
  
      HRESULT OpenFromFileName(   
   LPCOLESTR szFileName    
) throw( );  
```  
  
#### Parameters  
 `szFileName`  
 [in] The name of a file, usually a data source connection (.UDL) file.  
  
 For more information about data link files (.udl files), see [Data Link API Overview](https://msdn.microsoft.com/en-us/library/ms718102.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This method opens a data source object using the service components in oledb32.dll; this DLL contains the implementation of Service Components features such as Resource Pooling, Automatic Transaction Enlistment, and so on. For more information, see "OLE DB Services" in the OLE DB Programmer's Reference at [http://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/oledbole_db_services.asp?frame=true](http://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/oledbole_db_services.asp?frame=true).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDataSource Class](../vs140/CDataSource-Class.md)