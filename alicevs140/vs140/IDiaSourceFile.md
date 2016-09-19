---
title: "IDiaSourceFile"
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
ms.assetid: 6e9be757-797f-4960-ba62-c14092620bbd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSourceFile
Represents a source file.  
  
## Syntax  
  
```  
IDiaSourceFile : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaSourceFile`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaSourceFile::get_uniqueId](../vs140/IDiaSourceFile--get_uniqueId.md)|Retrieves a simple integer key value that is unique for this image.|  
|[IDiaSourceFile::get_fileName](../vs140/IDiaSourceFile--get_fileName.md)|Retrieves the source file name.|  
|[IDiaSourceFile::get_checksumType](../vs140/IDiaSourceFile--get_checksumType.md)|Retrieves the checksum type.|  
|[IDiaSourceFile::get_compilands](../vs140/IDiaSourceFile--get_compilands.md)|Retrieves an enumerator of the compilands with line numbers referencing this file.|  
|[IDiaSourceFile::get_checksum](../vs140/IDiaSourceFile--get_checksum.md)|Retrieves the checksum bytes.|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface by calling the [IDiaEnumSourceFiles::Item](../vs140/IDiaEnumSourceFiles--Item.md) or [IDiaEnumSourceFiles::Next](../vs140/IDiaEnumSourceFiles--Next.md) methods. See the example for details.  
  
## Example  
 This function displays the names of all source files contributing to the specified table.  
  
```cpp#  
void ShowSourceFiles(IDiaTable *pTable)  
{  
    CComPtr<IDiaEnumSourceFiles> pSourceFiles;  
    if ( SUCCEEDED( pTable->QueryInterface(  
                                _uuidof( IDiaEnumSourceFiles ),  
                               (void**)&pSourceFiles )  
                  )  
       )  
    {  
        CComPtr<IDiaSourceFile> pSourceFile;  
        while ( SUCCEEDED( hr = pSourceFiles->Next( 1, &pSourceFile, &celt ) ) &&  
                celt == 1 )  
        {  
            CDiaBSTR fileName;  
            if ( pSourceFile->get_fileName( &fileName) == S_OK )  
            {  
                printf( "file name: %ws\n", fileName );  
            }  
            pSourceFile = NULL;  
        }  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaEnumSourceFiles::Item](../vs140/IDiaEnumSourceFiles--Item.md)   
 [IDiaEnumSourceFiles::Next](../vs140/IDiaEnumSourceFiles--Next.md)   
 [IDiaLineNumber::get_sourceFile](../vs140/IDiaLineNumber--get_sourceFile.md)   
 [IDiaSession::findFileById](../vs140/IDiaSession--findFileById.md)   
 [IDiaSession::findLines](../vs140/IDiaSession--findLines.md)   
 [IDiaSession::findLinesByLinenum](../vs140/IDiaSession--findLinesByLinenum.md)