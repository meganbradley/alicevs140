---
title: "IDebugSymbolProvider::GetAddressesFromPosition"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1b0f02cb-8ace-4614-88f3-0e10239012b3
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSymbolProvider::GetAddressesFromPosition
This method maps a document position into an array of debug addresses.  
  
## Syntax  
  
```cpp#  
HRESULT GetAddressesFromPosition(   
   IDebugDocumentPosition2* pDocPos,  
   BOOL                     fStatmentOnly,  
   IEnumDebugAddresses**    ppEnumBegAddresses,  
   IEnumDebugAddresses**    ppEnumEndAddresses  
);  
```  
  
```c#  
int GetAddressesFromPosition(   
   IDebugDocumentPosition2  pDocPos,  
   bool                     fStatmentOnly,  
   out IEnumDebugAddresses  ppEnumBegAddresses,  
   out IEnumDebugAddresses  ppEnumEndAddresses  
);  
```  
  
#### Parameters  
 `pDocPos`  
 [in] The document position.  
  
 `fStatmentOnly`  
 [in] If TRUE, limits the debug addresses to a single statement.  
  
 `ppEnumBegAddresses`  
 [out] Returns an enumerator for the starting debug addresses associated with this statement or line.  
  
 `ppEnumEndAddresses`  
 [out] Returns an [IEnumDebugAddresses](../vs140/IEnumDebugAddresses.md) enumerator for the ending debug addresses associated with this statement or line.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A document position typically indicates a range of source lines. This method provides the starting and ending debug addresses associated with these lines. Some languages allow statements that span multiple lines, or lines that contains more than one statement. This method provides a flag to limit the debug addresses to a single statement.  
  
 It is possible for a single statement to have multiple debug addresses, as in the case of templates.  
  
## See Also  
 [IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md)   
 [GetAddressesFromContext](../vs140/IDebugSymbolProvider--GetAddressesFromContext.md)   
 [IEnumDebugAddresses](../vs140/IEnumDebugAddresses.md)