---
title: "IDiaSession::findLinesByLinenum"
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
ms.assetid: 76d5622d-9a91-4c2a-a98f-263af5d1daef
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findLinesByLinenum
Determines the line numbers of the compiland that the specified line number in a source file lies within or near.  
  
## Syntax  
  
```cpp#  
HRESULT findLinesByLinenum (   
   IDiaSymbol*           compiland,  
   IDiaSourceFile*       file,  
   DWORD                 linenum,  
   DWORD                 column,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### Parameters  
 `compiland`  
 [in] An [IDiaSymbol](../vs140/IDiaSymbol.md) object that represents the compiland in which to search for the line numbers. This parameter cannot be `NULL`.  
  
 `file`  
 [in] An [IDiaSourceFile](../vs140/IDiaSourceFile.md) object that represents the source file to search in. This parameter cannot be `NULL`.  
  
 `linenum`  
 [in] Specifies a one-based line number.  
  
> [!NOTE]
>  You cannot use zero to specify all lines (use the [IDiaSession::findLines](../vs140/IDiaSession--findLines.md) method to find all lines).  
  
 `column`  
 [in] Specifies the column number. Use zero to specify all columns. A column is a byte offset into a line.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md) objta that contains a list of the line numbers retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Example  
 The following example shows how to open a source file, enumerate the compilands contributed by this file, and locate the line numbers in the source file where each compiland starts.  
  
```cpp#  
void ShowLinesInCompilands(IDiaSession *pSession, LPCOLESTR filename)  
{  
    IDiaEnumSourceFiles* pEnum;  
    IDiaSourceFile*      pFile;  
    DWORD                celt;  
  
    pSession->findFile ( NULL, filename, nsFNameExt, &pEnum );  
    while ( pEnum->Next ( 1, &pFile, &celt ) == S_OK ) // for each file  
    {  
        IDiaEnumSymbols* pEnumCompilands;  
        IDiaSymbol* pCompiland;  
  
        pFile->get_compilands ( &pEnumCompilands );  
        // for each compiland  
        while ( pEnumCompilands->Next ( 1, &pCompiland, &celt ) == S_OK )  
        {  
            IDiaEnumLineNumbers* pEnum;  
            // Find first compiland closest to line 1 of the file.  
            if (pSession->findLinesByLinenum( pCompiland, pFile, 1, 0, &pEnum ) == S_OK)  
            {  
                IDiaLineNumber *pLineNumber;  
                DWORD lineCount;  
                while ( pEnum->Next(1,&pLineNumber,&lineCount) == S_OK)  
                {  
                     DWORD lineNum;  
                     if (pLineNumber->get_line(&lineNum) == S_OK)  
                     {  
                          printf("compiland starts in source at line number = %lu\n",lineNum);  
                     }  
                }  
            }  
        }  
    }  
}  
```  
  
## See Also  
 [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md)   
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaSession::findLinesByAddr](../vs140/IDiaSession--findLinesByAddr.md)   
 [IDiaSourceFile](../vs140/IDiaSourceFile.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)