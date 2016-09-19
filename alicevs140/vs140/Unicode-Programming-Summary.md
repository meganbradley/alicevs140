---
title: "Unicode Programming Summary"
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
ms.topic: article
ms.assetid: a4c9770f-6c9c-447c-996b-980920288bed
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Unicode Programming Summary
To take advantage of the MFC and C run-time support for Unicode, you need to:  
  
-   Define **_UNICODE**.  
  
     Define the symbol **_UNICODE** before you build your program.  
  
-   Specify entry point.  
  
     On the **Output** page of the Linker folder in the project's [Property Pages](../vs140/Property-Pages--Visual-C---.md) dialog box, set the Entry Point symbol to **wWinMainCRTStartup**.  
  
-   Use portable run-time functions and types.  
  
     Use the proper C run-time functions for Unicode string handling. You can use the **wcs** family of functions, but you might prefer the fully portable (internationally enabled) **_TCHAR** macros. These macros are all prefixed with **_tcs**; they substitute, one for one, for the **str** family of functions. These functions are described in detail in the [Internationalization](../vs140/Internationalization.md) section of the *Run-Time Library Reference*. For more information, see [Generic-Text Mappings in Tchar.h](../vs140/Generic-Text-Mappings-in-Tchar.h.md).  
  
     Use **_TCHAR** and the related portable data types described in [Support for Unicode](../vs140/Support-for-Unicode.md).  
  
-   Handle literal strings properly.  
  
     The Visual C++ compiler interprets a literal string coded as:  
  
    ```  
    L"this is a literal string"  
    ```  
  
     to mean a string of Unicode characters. You can use the same prefix for literal characters. Use the **_T** macro to code literal strings generically, so they compile as Unicode strings under Unicode or as ANSI strings (including MBCS) without Unicode. For example, instead of:  
  
    ```  
    pWnd->SetWindowText( "Hello" );  
    ```  
  
     use:  
  
    ```  
    pWnd->SetWindowText( _T("Hello") );  
    ```  
  
     With **_UNICODE** defined, **_T** translates the literal string to the L-prefixed form; otherwise, **_T** translates the string without the L prefix.  
  
    > [!TIP]
    >  The **_T** macro is identical to the `_TEXT` macro.  
  
-   Be careful passing string lengths to functions.  
  
     Some functions want the number of characters in a string; others want the number of bytes. For example, if **_UNICODE** is defined, the following call to a `CArchive` object will not work (`str` is a `CString`):  
  
    ```  
    archive.Write( str, str.GetLength( ) );    // invalid  
    ```  
  
     In a Unicode application, the length gives you the number of characters but not the correct number of bytes, because each character is 2 bytes wide. Instead, you must use:  
  
    ```  
    archive.Write( str, str.GetLength( ) * sizeof( _TCHAR ) );    // valid  
    ```  
  
     which specifies the correct number of bytes to write.  
  
     However, MFC member functions that are character-oriented, rather than byte-oriented, work without this extra coding:  
  
    ```  
    pDC->TextOut( str, str.GetLength( ) );  
    ```  
  
     `CDC::TextOut` takes a number of characters, not a number of bytes.  
  
-   Use [fopen_s, _wfopen_s](../Topic/fopen_s,%20_wfopen_s.md) to open Unicode files.  
  
 To summarize, MFC and the run-time library provide the following support for Unicode programming under Windows 2000:  
  
-   Except for database class member functions, all MFC functions are Unicode-enabled, including `CString`. `CString` also provides Unicode/ANSI conversion functions.  
  
-   The run-time library supplies Unicode versions of all string-handling functions. (The run-time library also supplies portable versions suitable for Unicode or for MBCS. These are the **_tcs** macros.)  
  
-   Tchar.h supplies portable data types and the **_T** macro for translating literal strings and characters. For more information, see [Generic-Text Mappings in Tchar.h](../vs140/Generic-Text-Mappings-in-Tchar.h.md).  
  
-   The run-time library provides a wide-character version of **main**. Use **wmain** to make your application Unicode-aware.  
  
## See Also  
 [Support for Unicode](../vs140/Support-for-Unicode.md)