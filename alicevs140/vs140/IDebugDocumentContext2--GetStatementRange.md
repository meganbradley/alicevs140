---
title: "IDebugDocumentContext2::GetStatementRange"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bc94851a-0ec4-47ea-99c7-0a585e54e726
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentContext2::GetStatementRange
Gets the file statement range of the document context.  
  
## Syntax  
  
```cpp#  
HRESULT GetStatementRange(   
   TEXT_POSITION* pBegPosition,  
   TEXT_POSITION* pEndPosition  
);  
```  
  
```c#  
int GetStatementRange(   
   TEXT_POSITION[] pBegPosition,  
   TEXT_POSITION[] pEndPosition  
);  
```  
  
#### Parameters  
 `pBegPosition`  
 [in, out] A [TEXT_POSITION](../vs140/TEXT_POSITION.md) structure that is filled in with the starting position. Set this argument to a null value if this information is not needed.  
  
 `pEndPosition`  
 [in, out] A [TEXT_POSITION](../vs140/TEXT_POSITION.md) structure that is filled in with the ending position. Set this argument to a null value if this information is not needed.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A statement range is the range of the lines that contributed the code to which this document context refers.  
  
 To obtain the range of source code (including comments) within this document context, call the [GetSourceRange](../vs140/IDebugDocumentContext2--GetSourceRange.md) method.  
  
## Example  
 The following example shows how to implement this method for a simple `CDebugContext` object that exposes the [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md) interface. This example fills in the ending position only if the beginning position is not a null value.  
  
```cpp#  
HRESULT CDebugContext::GetStatementRange(TEXT_POSITION* pBegPosition,  
                                         TEXT_POSITION* pEndPosition)    
{    
   HRESULT hr;    
  
   // Check for a valid beginning position argument pointer.    
   if (pBegPosition)    
   {    
      // Copy the member TEXT_POSITION into the local pBegPosition.    
      memcpy(pBegPosition, &m_pos, sizeof (TEXT_POSITION));    
  
      // Check for a valid ending position argument pointer.   
     if (pEndPosition)    
      {    
         // Copy the member TEXT_POSITION into the local pEndPosition.    
         memcpy(pEndPosition, &m_pos, sizeof (TEXT_POSITION));    
      }    
      hr = S_OK;    
   }    
   else    
   {    
      hr = E_INVALIDARG;    
   }    
  
   return hr;    
}    
```  
  
## See Also  
 [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md)   
 [GetSourceRange](../vs140/IDebugDocumentContext2--GetSourceRange.md)   
 [TEXT_POSITION](../vs140/TEXT_POSITION.md)