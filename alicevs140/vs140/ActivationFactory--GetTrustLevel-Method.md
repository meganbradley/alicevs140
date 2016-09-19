---
title: "ActivationFactory::GetTrustLevel Method"
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
ms.assetid: 31547ae6-d2ab-4039-923c-154d53fb1a8b
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ActivationFactory::GetTrustLevel Method
Gets the trust level of the object that the current ActivationFactory instantiates.  
  
## Syntax  
  
```  
STDMETHOD(  
   GetTrustLevel  
)(_Out_ TrustLevel* trustLvl);  
```  
  
#### Parameters  
 `trustLvl`  
 When this operation completes, the trust level of the runtime class that the ActivationFactory instantiates.  
  
## Return Value  
 S_OK if successful; otherwise, an assertion error is emitted and `trustLvl` is set to FullTrust.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ActivationFactory Class](../vs140/ActivationFactory-Class.md)