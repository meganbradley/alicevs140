---
title: "IDiaLineNumber::get_sourceFile"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86fc4411-375e-4b99-8f96-4da2c3f68190
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLineNumber::get_sourceFile
Retrieves a reference to the source file.  
  
## Syntax  
  
```cpp#  
HRESULT get_sourceFile (   
   IDiaSourceFile** pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns an [IDiaSourceFile](../vs140/IDiaSourceFile.md) object that represents the source file.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if this property is not supported. Otherwise, returns an error code.  
  
## See Also  
 [IDiaLineNumber](../vs140/IDiaLineNumber.md)   
 [IDiaSourceFile](../vs140/IDiaSourceFile.md)