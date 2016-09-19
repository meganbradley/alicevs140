---
title: "directory_options Enumeration"
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
ms.assetid: cabb8a38-3916-48e3-9d3c-514f29b90f4b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# directory_options Enumeration
Specifies whether to follow symbolic links to directories or to ignore them.  
  
## Syntax  
  
```cpp  
enum class directory_options {  
    none = 0,  
    follow_directory_symlink  
    };  
```  
  
## Members  
  
|Name|Description|  
|----------|-----------------|  
|`none`|Default behavior: ignore symbolic links to directories. Permission denied is an error.|  
|`follow_directory_symlink`|Treat symbolic links to directories as actual directories.|  
  
## See Also  
 [<filesystem\>](../vs140/-filesystem-.md)