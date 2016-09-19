---
title: "CDumpContext::HexDump"
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
ms.topic: reference
ms.assetid: df7500c0-c6bd-4d93-9853-d563221dad8c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDumpContext::HexDump
Dumps an array of bytes formatted as hexadecimal numbers.  
  
## Syntax  
  
```  
  
      void HexDump(  
   LPCTSTR lpszLine,  
   BYTE* pby,  
   int nBytes,  
   int nWidth   
);  
```  
  
#### Parameters  
 *lpszLine*  
 A string to output at the start of a new line.  
  
 *pby*  
 A pointer to a buffer containing the bytes to dump.  
  
 `nBytes`  
 The number of bytes to dump.  
  
 `nWidth`  
 Maximum number of bytes dumped per line (not the width of the output line).  
  
## Remarks  
 To dump a single, specific item type as a hexadecimal number, call [CDumpContext::DumpAsHex](../vs140/CDumpContext--DumpAsHex.md).  
  
## Example  
 [!CODE [NVC_MFC_Utilities#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#15)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CDumpContext Class](../vs140/CDumpContext-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)