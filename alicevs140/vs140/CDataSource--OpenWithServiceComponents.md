---
title: "CDataSource::OpenWithServiceComponents"
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
ms.assetid: 49c1d037-36ae-4fde-8e54-ced623abe1a9
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataSource::OpenWithServiceComponents
Opens a data source object using the service components in oledb32.dll.  
  
## Syntax  
  
```  
  
      HRESULT OpenWithServiceComponents (  
   const CLSID clsid,  
   DBPROPSET* pPropset = NULL,  
   ULONG ulPropSets = 1   
);  
HRESULT OpenWithServiceComponents (  
   LPCSTR szProgID,  
   DBPROPSET* pPropset = NULL,  
   ULONG ulPropSets = 1   
);  
```  
  
#### Parameters  
 `clsid`  
 [in] The **CLSID** of a data provider.  
  
 `szProgID`  
 [in] Program ID of a data provider.  
  
 `pPropset`  
 [in] A pointer to an array of [DBPROPSET](https://msdn.microsoft.com/en-us/library/ms714367.aspx) structures containing properties and values to be set. See [Property Sets and Property Groups](https://msdn.microsoft.com/en-us/library/ms713696.aspx) in the *OLE DB Programmer's Reference* in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. If the data source object is initialized, the properties must belong to the Data Source property group. If the same property is specified more than once in `pPropset`, then which value is used is provider-specific. If `ulPropSets` is zero, this parameter is ignored.  
  
 `ulPropSets`  
 [in] The number of [DBPROPSET](https://msdn.microsoft.com/en-us/library/ms714367.aspx) structures passed in the *pPropSet* argument. If this is zero, the provider ignores `pPropset`.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This method opens a data source object using the service components in oledb32.dll; this DLL contains the implementation of Service Components features such as Resource Pooling, Automatic Transaction Enlistment, and so on. For more information, see "OLE DB Services" in the OLE DB Programmer's Reference at [http://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/oledbole_db_services.asp?frame=true](http://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/oledbole_db_services.asp?frame=true).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDataSource Class](../vs140/CDataSource-Class.md)