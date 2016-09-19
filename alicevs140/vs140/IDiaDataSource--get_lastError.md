---
title: "IDiaDataSource::get_lastError"
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
ms.assetid: cf08850b-8b75-4e8c-90bd-bd0214756f99
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaDataSource::get_lastError
Retrieves the file name for the last load error.  
  
## Syntax  
  
```cpp#  
HRESULT get_lastError (  
   BSTR* pRetVal  
);  
```  
  
#### Parameters  
 pRetVal  
 [out] Returns a string that contains the .pdb file name associated with the last load error.  
  
## Return Value  
 Returns the last error code caused by a load operation. Returns `E_INVALIDARG` if the `pRetVal` parameter is `NULL`.  
  
## Example  
  
```cpp#  
BSTR    fileName;  
HRESULT errorCode = pSource->get_lastError( &fileName );  
```  
  
## See Also  
 [IDiaDataSource](../vs140/IDiaDataSource.md)