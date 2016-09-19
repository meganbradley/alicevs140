---
title: "Last Character in a String"
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
ms.assetid: 0a180376-4e55-41e8-9c64-539c7b6d8047
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Last Character in a String
Use the following tips:  
  
-   Trail byte ranges overlap the ASCII character set in many cases. You can safely use bytewise scans for any control characters (less than 32).  
  
-   Consider the following line of code, which might be checking to see if the last character in a string is a backslash character:  
  
    ```  
    if ( sz[ strlen( sz ) - 1 ] == '\\' )    // Is last character a '\'?  
        // . . .  
    ```  
  
     Because `strlen` is not MBCS-aware, it returns the number of bytes, not the number of characters, in a multibyte string. Also, note that in some code pages (932, for example), '\\' (0x5c) is a valid trail byte (`sz` is a C string).  
  
     One possible solution is to rewrite the code this way:  
  
    ```  
    char *pLast;  
    pLast = _mbsrchr( sz, '\\' );    // find last occurrence of '\' in sz  
    if ( pLast && ( *_mbsinc( pLast ) == '\0' ) )  
        // . . .  
    ```  
  
     This code uses the MBCS functions `_mbsrchr` and `_mbsinc`. Because these functions are MBCS-aware, they can distinguish between a '\\' character and a trail byte '\\'. The code performs some action if the last character in the string is a null ('\0').  
  
## See Also  
 [MBCS Programming Tips](../vs140/MBCS-Programming-Tips.md)   
 [Character Assignment](../vs140/Character-Assignment.md)