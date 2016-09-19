---
title: "CDumpContext::DumpAsHex"
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
ms.assetid: 2f7f1b45-d83f-44da-af7b-5d5356cadc50
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDumpContext::DumpAsHex
Dumps the specified type formatted as hexadecimal numbers.  
  
## Syntax  
  
```  
  
      CDumpContext& DumpAsHex(   
   BYTE b   
);  
CDumpContext& DumpAsHex(   
   DWORD dw   
);  
CDumpContext& DumpAsHex(   
   int n   
);  
CDumpContext& DumpAsHex(   
   LONG l   
);  
CDumpContext& DumpAsHex(   
   LONGLONG n   
);  
CDumpContext& DumpAsHex(   
   UINT u   
);  
CDumpContext& DumpAsHex(   
   ULONGLONG n   
);  
CDumpContext& DumpAsHex(   
   WORD w   
);  
```  
  
## Return Value  
 A reference to a `CDumpContext` object.  
  
## Remarks  
 Call this member function to dump the item of the specified type as a hexadecimal number. To dump an array, call [CDumpContext::HexDump](../vs140/CDumpContext--HexDump.md).  
  
## Example  
 [!CODE [NVC_MFC_Utilities#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#13)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CDumpContext Class](../vs140/CDumpContext-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDumpContext::operator <<](../vs140/CDumpContext--operator---.md)