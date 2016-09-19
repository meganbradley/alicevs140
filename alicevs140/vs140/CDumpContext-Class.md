---
title: "CDumpContext Class"
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
ms.assetid: 98c52b2d-14b5-48ed-b423-479a4d1c60fa
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDumpContext Class
Supports stream-oriented diagnostic output in the form of human-readable text.  
  
## Syntax  
  
```  
class CDumpContext  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CDumpContext::CDumpContext](#cdumpcontext__cdumpcontext)|Constructs a `CDumpContext` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CDumpContext::DumpAsHex](#cdumpcontext__dumpashex)|Dumps the indicated item in hexadecimal format.|  
|[CDumpContext::Flush](#cdumpcontext__flush)|Flushes any data in the dump context buffer.|  
|[CDumpContext::GetDepth](#cdumpcontext__getdepth)|Gets an integer corresponding to the depth of the dump.|  
|[CDumpContext::HexDump](#cdumpcontext__hexdump)|Dumps bytes contained in an array in hexadecimal format.|  
|[CDumpContext::SetDepth](#cdumpcontext__setdepth)|Sets the depth of the dump.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CDumpContext::operator<<](#cdumpcontext__operator__lt__lt_)|Inserts variables and objects into the dump context.|  
  
## Remarks  
 `CDumpContext` does not have a base class.  
  
 You can use [afxDump](../vs140/afxDump--CDumpContext-in-MFC-.md), a predeclared `CDumpContext` object, for most of your dumping. The `afxDump` object is available only in the Debug version of the Microsoft Foundation Class Library.  
  
 Several of the memory [diagnostic services](../vs140/Diagnostic-Services.md) use `afxDump` for their output.  
  
 Under the Windows environment, the output from the predefined `afxDump` object, conceptually similar to the `cerr` stream, is routed to the debugger via the Windows function **OutputDebugString**.  
  
 The `CDumpContext` class has an overloaded insertion ( **<<**) operator for `CObject` pointers that dumps the object's data. If you need a custom dump format for a derived object, override [CObject::Dump](../vs140/CObject-Class.md#cobject__dump). Most Microsoft Foundation classes implement an overridden `Dump` member function.  
  
 Classes that are not derived from `CObject`, such as `CString`, `CTime`, and `CTimeSpan`, have their own overloaded `CDumpContext` insertion operators, as do often-used structures such as **CFileStatus**, `CPoint`, and `CRect`.  
  
 If you use the [IMPLEMENT_DYNAMIC](../vs140/IMPLEMENT_DYNAMIC.md) or [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md) macro in the implementation of your class, then `CObject::Dump` will print the name of your `CObject`-derived class. Otherwise, it will print `CObject`.  
  
 The `CDumpContext` class is available with both the Debug and Release versions of the library, but the `Dump` member function is defined only in the Debug version. Use **#ifdef _DEBUG** / `#endif` statements to bracket your diagnostic code, including your custom `Dump` member functions.  
  
 Before you create your own `CDumpContext` object, you must create a `CFile` object that serves as the dump destination.  
  
 For more information on `CDumpContext`, see [Debugging MFC Applications](../vs140/MFC-Debugging-Techniques.md).  
  
 **#define _DEBUG**  
  
## Inheritance Hierarchy  
 `CDumpContext`  
  
## Requirements  
 **Header:** afx.h  
  
##  <a name="cdumpcontext__cdumpcontext"></a>  CDumpContext::CDumpContext  
 Constructs an object of class `CDumpContext`.  
  
```  
CDumpContext(    CFile* pFile = NULL );  
  
```  
  
### Parameters  
 `pFile`  
 A pointer to the `CFile` object that is the dump destination.  
  
### Remarks  
 The `afxDump` object is constructed automatically.  
  
 Do not write to the underlying `CFile` while the dump context is active; otherwise, you will interfere with the dump. Under the Windows environment, the output is routed to the debugger via the Windows function **OutputDebugString**.  
  
### Example  
 [!CODE [NVC_MFC_Utilities#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#12)]  
  
##  <a name="cdumpcontext__dumpashex"></a>  CDumpContext::DumpAsHex  
 Dumps the specified type formatted as hexadecimal numbers.  
  
```  
CDumpContext& DumpAsHex(    BYTE  b ); CDumpContext& DumpAsHex(    DWORD  dw ); CDumpContext& DumpAsHex(    int  n ); CDumpContext& DumpAsHex(    LONG  l ); CDumpContext& DumpAsHex(    LONGLONG  n ); CDumpContext& DumpAsHex(    UINT  u ); CDumpContext& DumpAsHex(    ULONGLONG  n ); CDumpContext& DumpAsHex(    WORD  w );  
  
```  
  
### Return Value  
 A reference to a `CDumpContext` object.  
  
### Remarks  
 Call this member function to dump the item of the specified type as a hexadecimal number. To dump an array, call [CDumpContext::HexDump](#cdumpcontext__hexdump).  
  
### Example  
  [!CODE [NVC_MFC_Utilities#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#13)]  
  
##  <a name="cdumpcontext__flush"></a>  CDumpContext::Flush  
 Forces any data remaining in buffers to be written to the file attached to the dump context.  
  
```  
void Flush( );  
  
```  
  
### Example  
 [!CODE [NVC_MFC_Utilities#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#14)]  
  
##  <a name="cdumpcontext__getdepth"></a>  CDumpContext::GetDepth  
 Determines whether a deep or shallow dump is in process.  
  
```  
int GetDepth( ) const;  
  
```  
  
### Return Value  
 The depth of the dump as set by `SetDepth`.  
  
### Example  
  See the example for [SetDepth](#cdumpcontext__setdepth).  
  
##  <a name="cdumpcontext__hexdump"></a>  CDumpContext::HexDump  
 Dumps an array of bytes formatted as hexadecimal numbers.  
  
```  
void HexDump(    LPCTSTR lpszLine ,    BYTE* pby ,    int nBytes ,    int nWidth );  
  
```  
  
### Parameters  
 *lpszLine*  
 A string to output at the start of a new line.  
  
 *pby*  
 A pointer to a buffer containing the bytes to dump.  
  
 `nBytes`  
 The number of bytes to dump.  
  
 `nWidth`  
 Maximum number of bytes dumped per line (not the width of the output line).  
  
### Remarks  
 To dump a single, specific item type as a hexadecimal number, call [CDumpContext::DumpAsHex](#cdumpcontext__dumpashex).  
  
### Example  
  [!CODE [NVC_MFC_Utilities#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#15)]  
  
##  <a name="cdumpcontext__operator__lt__lt_"></a>  CDumpContext::operator &lt;&lt;  
 Outputs the specified data to the dump context.  
  
```  
CDumpContext& operator <<(    const CObject* pOb ); throw(    CFileException*  ); CDumpContext& operator <<(    const CObject& ob ); throw(    CFileException*  ); CDumpContext& operator <<(    LPCTSTR lpsz ); throw(    CFileException*  ); CDumpContext& operator <<(    const void* lp ); throw(    CFileException*  ); CDumpContext& operator <<(    BYTE by ); throw(    CFileException*  ); CDumpContext& operator <<(    WORD w ); throw(    CFileException*  ); CDumpContext& operator <<(    DWORD dw ); throw(    CFileException*  ); CDumpContext& operator <<(    int n ); throw(    CFileException*  ); CDumpContext& operator <<(    double d ); throw(    CFileException*  ); CDumpContext& operator <<(    float f ); throw(    CFileException*  ); CDumpContext& operator <<(    LONG l ); throw(    CFileException*  ); CDumpContext& operator <<(    UINT u ); throw(    CFileException*  ); CDumpContext& operator <<(    LPCWSTR lpsz ); throw(    CFileException*  ); CDumpContext& operator <<(    LPCSTR lpsz ); throw(    CFileException*  ); CDumpContext& operator <<(    LONGLONG  n ); CDumpContext& operator <<(    ULONGLONG  n ); CDumpContext& operator <<(    HWND  h ); CDumpContext& operator <<( HDC  h ); CDumpContext& operator <<( HMENU  h ); CDumpContext& operator <<( HACCEL  h ); CDumpContext& operator <<( HFONT  h );  
  
```  
  
### Return Value  
 A `CDumpContext` reference. Using the return value, you can write multiple insertions on a single line of source code.  
  
### Remarks  
 The insertion operator is overloaded for `CObject` pointers as well as for most primitive types. A pointer to character results in a dump of string contents; a pointer to `void` results in a hexadecimal dump of the address only. A **LONGLONG** results in a dump of a 64-bit signed integer; A **ULONGLONG** results in a dump of a 64-bit unsigned integer.  
  
 If you use the `IMPLEMENT_DYNAMIC` or `IMPLEMENT_SERIAL` macro in the implementation of your class, then the insertion operator, through `CObject::Dump`, will print the name of your `CObject`-derived class. Otherwise, it will print `CObject`. If you override the `Dump` function of the class, then you can provide a more meaningful output of the object's contents instead of a hexadecimal dump.  
  
### Example  
 [!CODE [NVC_MFC_Utilities#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#17)]  
  
##  <a name="cdumpcontext__setdepth"></a>  CDumpContext::SetDepth  
 Sets the depth for the dump.  
  
```  
void SetDepth(    int nNewDepth );  
  
```  
  
### Parameters  
 *nNewDepth*  
 The new depth value.  
  
### Remarks  
 If you are dumping a primitive type or simple `CObject` that contains no pointers to other objects, then a value of 0 is sufficient. A value greater than 0 specifies a deep dump where all objects are dumped recursively. For example, a deep dump of a collection will dump all elements of the collection. You may use other specific depth values in your derived classes.  
  
> [!NOTE]
>  Circular references are not detected in deep dumps and can result in infinite loops.  
  
### Example  
 [!CODE [NVC_MFC_Utilities#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#16)]  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile](../vs140/CFile-Class.md)   
 [CObject](../vs140/CObject-Class.md)