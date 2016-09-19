---
title: "IDiaDataSource::loadDataFromIStream"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8fe33eea-1457-4b8c-ae19-f1ede5578483
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaDataSource::loadDataFromIStream
Prepares the debug data stored in a program database (.pdb) file accessed through an in-memory data stream.  
  
## Syntax  
  
```cpp#  
HRESULT loadDataFromIStream (   
   IStream* pIStream  
);  
```  
  
#### Parameters  
 pIStream  
 [in] An <xref:IStream?qualifyHint=False> object representing the data stream to use.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The following table shows the possible return values for this method.  
  
|Value|Description|  
|-----------|-----------------|  
|E_PDB_FORMAT|Attempted to access a file with an obsolete format.|  
|E_INVALIDARG|Invalidparameter.|  
|E_UNEXPECTED|Data source has already been prepared.|  
  
## Remarks  
 This method allows the debug data for an executable to be obtained from memory through an <xref:IStream?qualifyHint=False> object.  
  
 To load a .pdb file without validation, use the [IDiaDataSource::loadDataFromPdb](../vs140/IDiaDataSource--loadDataFromPdb.md) method.  
  
 To validate the .pdb file against specific criteria, use the [IDiaDataSource::loadAndValidateDataFromPdb](../vs140/IDiaDataSource--loadAndValidateDataFromPdb.md) method.  
  
 To gain access to the data load process (through a callback mechanism), use the [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md) method.  
  
## See Also  
 [IDiaDataSource](../vs140/IDiaDataSource.md)   
 [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md)   
 [IDiaDataSource::loadDataFromPdb](../vs140/IDiaDataSource--loadDataFromPdb.md)   
 [IDiaDataSource::loadAndValidateDataFromPdb](../vs140/IDiaDataSource--loadAndValidateDataFromPdb.md)