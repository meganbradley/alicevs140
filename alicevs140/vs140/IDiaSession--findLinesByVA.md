---
title: "IDiaSession::findLinesByVA"
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
ms.assetid: f647eee9-a73c-483b-9fe9-21f42e560a7b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findLinesByVA
Retrieves the line number information for lines contained in a specified virtual address (VA) range.  
  
## Syntax  
  
```cpp#  
HRESULT findLinesByVA (   
   ULONGLONG             va,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### Parameters  
 `va`  
 [in] Specifies the address as a VA.  
  
 `length`  
 [in] Specifies the number of bytes of address range to cover with this query.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md) object that contains a list of all the line numbers that cover the specified address range.  
  
## Example  
 This example shows a function that obtains all line numbers contained in a function using the function's virtual address and length.  
  
```cpp#  
IDiaEnumLineNumbers *GetLineNumbersByVA(IDiaSymbol *pFunc, IDiaSession *pSession)  
{  
    IDiaEnumLineNumbers* pEnum = NULL;  
    ULONGLONG            va;  
    ULONGLONG            length;  
  
    if (pFunc->get_virtualAddress ( &va ) == S_OK)  
    {  
        pFunc->get_length( &length );  
        pSession->findLinesByVA( va, static_cast<DWORD>( length ), &pEnum );  
    }  
    return(pEnum);  
}  
```  
  
## See Also  
 [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md)   
 [IDiaSession](../vs140/IDiaSession.md)