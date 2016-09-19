---
title: "accelerator::accelerator Constructor"
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
ms.assetid: 6c560bd9-7fc0-4b19-a55a-4d8d6b6f686d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator::accelerator Constructor
Initializes a new instance of the [accelerator class](../vs140/accelerator-Class.md).  
  
## Syntax  
  
```  
accelerator();  
  
explicit accelerator(  
   const std::wstring &_Device_path  
);  
  
accelerator(  
   const accelerator &_Other  
);  
```  
  
#### Parameters  
 `_Device_path`  
 The path of the physical device.  
  
 `_Other`  
 The accelerator to copy.  
  
## Overload List  
  
|||  
|-|-|  
|Name|Description|  
|`accelerator();`|Initializes a new instance of the `accelerator` class. The new instance represents the default accelerator, usually  the fastest accelerator available. This constructor is equivalent the constructor `accelerator(accelerator::default_accelerator)`.|  
|`explicit accelerator(    const std::wstring &_Device_path);`|Initializes a new instance of the `accelerator` class. The new instance represents the physical device specified in the path argument. The path can be any one of the following:<br /><br /> [accelerator::default_accelerator Data Member](../vs140/accelerator--default_accelerator-Data-Member.md) or `L""`, which represents the path of the fastest accelerator available, as chosen by the runtime.<br /><br /> [accelerator::direct3d_warp Data Member](../vs140/accelerator--direct3d_warp-Data-Member.md) or `L"direct3d\\warp"`, which represents the WARP accelerator.<br /><br /> [accelerator::direct3d_ref Data Member](../vs140/accelerator--direct3d_ref-Data-Member.md) or `L"direct3d\\ref"`, which represents the REF accelerator.<br /><br /> A device path that uniquely identifies a hardware accelerator that is available on the host system.|  
|`accelerator(   const accelerator &_Other);`|Initializes a new instance of the `accelerator` class. The new instance is a copy of another `accelerator` object. This constructor performs a shallow copy. The new `accelerator` object points to the same underlying device that is specified in the `accelerator` parameter.|  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator Class](../vs140/accelerator-Class.md)