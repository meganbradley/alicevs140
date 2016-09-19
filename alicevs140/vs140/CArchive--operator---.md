---
title: "CArchive::operator &lt;&lt;"
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
ms.assetid: 0870b7b5-7d3a-424f-a59f-824a39a119e0
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::operator &lt;&lt;
Stores the indicated object or primitive type to the archive.  
  
## Syntax  
  
```  
  
      friend CArchive& operator <<(  
   CArchive& ar,  
   const CObject* pOb   
);  
throw(  
   CArchiveException*,  
   CFileException*   
);  
CArchive& AFXAPI operator <<(   
   CArchive& ar,  
   const RECT& rect  
);  
CArchive& AFXAPI operator <<(   
   CArchive& ar,   
   POINT point   
);  
CArchive& AFXAPI operator <<(   
  CArchive& ar,   
   SIZE size   
);  
template<    
   typename BaseType,    
   class StringTraits    
>   
CArchive& operator<<(   
   const ATL::CStringT<   
      BaseType,    
      StringTraits   
   >& str   
);  
CArchive& operator <<(  
   BYTE by   
);  
CArchive& operator <<(  
   WORD w   
);  
CArchive& operator <<(  
   LONG l   
);  
CArchive& operator <<(  
   DWORD dw   
);  
CArchive& operator <<(  
   float f   
);  
CArchive& operator <<(  
   double d   
);  
CArchive& operator <<(  
   int i   
);  
CArchive& operator <<(  
   short w   
);  
CArchive& operator <<(  
   char ch   
);  
CArchive& operator<<(   
   wchar_t ch    
);  
CArchive& operator <<(  
   unsigned u   
);  
CArchive& operator <<(  
   bool b   
);  
CArchive& operator<<(   
   ULONGLONG dwdw    
);  
CArchive& operator<<(   
   LONGLONG dwdw    
);  
```  
  
## Return Value  
 A `CArchive` reference that enables multiple insertion operators on a single line.  
  
## Remarks  
 The last two versions above are specifically for storing 64-bit integers.  
  
 If you used the `IMPLEMENT_SERIAL` macro in your class implementation, then the insertion operator overloaded for `CObject` calls the protected **WriteObject**. This function, in turn, calls the `Serialize` function of the class.  
  
 The [CStringT](../vs140/CStringT-Class.md) insertion operator (<<) supports diagnostic dumping and storing to an archive.  
  
## Example  
 This example demonstrates the use of the `CArchive` insertion operator << with the `int` and `long` types.  
  
 [!CODE [NVC_MFCSerialization#31](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#31)]  
  
## Example  
 This example 2 demonstrates the use of the `CArchive` insertion operator << with the `CStringT` type.  
  
 [!CODE [NVC_MFCSerialization#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#32)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::WriteObject](../vs140/CArchive--WriteObject.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)   
 [CStringT Class](../vs140/CStringT-Class.md)   
 [CDumpContext Class](../vs140/CDumpContext-Class.md)