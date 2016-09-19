---
title: "__addgsbyte, __addgsword, __addgsdword, __addgsqword"
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
ms.assetid: 4fa03e69-d849-49ed-ba37-1d3aa23c2a21
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __addgsbyte, __addgsword, __addgsdword, __addgsqword
**Microsoft Specific**  
  
 Add a value to a memory location specified by an offset relative to the beginning of the `GS` segment.  
  
## Syntax  
  
```  
void __addgsbyte(   
   unsigned long Offset,   
   unsigned char Data   
);  
void __addgsword(   
   unsigned long Offset,   
   unsigned short Data   
);  
void __addgsdword(   
   unsigned long Offset,   
   unsigned long Data   
);  
void __addgsqword(   
   unsigned long Offset,   
   unsigned __int64 Data   
);  
```  
  
#### Parameters  
 [in] `Offset`  
 The offset from the beginning of `GS`.  
  
 [in] `Data`  
 The value to add to the memory location.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__addgsbyte`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
|`__addgsword`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
|`__addgsdword`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
|`__addgsqword`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
## Remarks  
 These intrinsics are available in kernel mode only, and these routines are only available as intrinsics.  
  
## END Microsoft Specific  
  
## See Also  
 [__incgsbyte, \__incgsword, \__incgsdword, \__incgsqword](../vs140/__incgsbyte--__incgsword--__incgsdword--__incgsqword.md)   
 [__readgsbyte, \__readgsdword, \__readgsqword, \__readgsword](../vs140/__readgsbyte--__readgsdword--__readgsqword--__readgsword.md)   
 [__writegsbyte, \__writegsdword, \__writegsqword, \__writegsword](../vs140/__writegsbyte--__writegsdword--__writegsqword--__writegsword.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)