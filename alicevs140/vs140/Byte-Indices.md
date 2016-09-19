---
title: "Byte Indices"
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
ms.assetid: f6e7774a-86c6-41c2-89e3-74fd46432e47
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Byte Indices
Use the following tips:  
  
-   Working with a bytewise index into a string presents problems similar to those posed by pointer manipulation. Consider this example, which scans a string for a backslash character:  
  
    ```  
    while ( rgch[ i ] != '\\' )  
        i++;  
    ```  
  
     This might index a trail byte, not a lead byte, and thus it might not point to a `character`.  
  
-   Use the [_mbclen](../vs140/_mbclen--mblen--_mblen_l.md) function to solve the preceding problem:  
  
    ```  
    while ( rgch[ i ] != '\\' )  
        i += _mbclen ( rgch + i );  
    ```  
  
     This correctly indexes to a lead byte, hence to a `character`. The `_mbclen` function determines the size of a character (1 or 2 bytes).  
  
## See Also  
 [MBCS Programming Tips](../vs140/MBCS-Programming-Tips.md)   
 [Last Character in a String](../vs140/Last-Character-in-a-String.md)