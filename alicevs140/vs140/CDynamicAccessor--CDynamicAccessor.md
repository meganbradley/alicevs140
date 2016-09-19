---
title: "CDynamicAccessor::CDynamicAccessor"
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
ms.assetid: bf40fe81-2c85-473e-9075-51ad9b060b39
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicAccessor::CDynamicAccessor
Instantiates and initializes the `CDynamicAccessor` object.  
  
## Syntax  
  
```  
  
      CDynamicAccessor(   
   DBBLOBHANDLINGENUM eBlobHandling = DBBLOBHANDLING_DEFAULT,   
   DBLENGTH nBlobSize = 8000   
);  
```  
  
#### Parameters  
 `eBlobHandling`  
 Specifies how the binary large object (BLOB) data is to be handled. The default value is **DBBLOBHANDLING_DEFAULT**. See [SetBlobHandling](../vs140/CDynamicAccessor--SetBlobHandling.md) for a description of the **DBBLOBHANDLINGENUM** values.  
  
 `nBlobSize`  
 The maximum BLOB size in bytes; column data over this value is treated as a BLOB. The default value is 8,000. See [SetBlobSizeLimit](../vs140/CDynamicAccessor--SetBlobSizeLimit.md) for details.  
  
## Remarks  
 If you use the constructor to initialize the `CDynamicAccessor` object, you can specify how it will bind BLOBs. BLOBs can contain binary data such as graphics, sound, or compiled code. The default behavior is to treat columns more than 8,000 bytes as BLOBs and try to bind them to an `ISequentialStream` object. However, you can specify a different value to be the BLOB size.  
  
 You can also specify how `CDynamicAccessor` handles column data that qualifies as BLOB data: it can handle BLOB data in the default manner; it can skip (does not bind) BLOB data; or it can bind BLOB data in provider-allocated memory.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)