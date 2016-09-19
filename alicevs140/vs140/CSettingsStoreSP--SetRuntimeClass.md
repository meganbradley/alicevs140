---
title: "CSettingsStoreSP::SetRuntimeClass"
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
ms.assetid: eb6f0424-bbd3-4635-96d3-308f3372739a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSettingsStoreSP::SetRuntimeClass
Sets the runtime class. The method [CSettingsStoreSP::Create](../vs140/CSettingsStoreSP--Create.md) uses the runtime class to determine what type of object to create.  
  
## Syntax  
  
```  
static BOOL __stdcall CSettingsStoreSP::SetRuntimeClass(  
   CRuntimeClass* pRTI  
);  
```  
  
#### Parameters  
 [in] `pRTI`  
 A pointer to the runtime class information for a class derived from the [CSettingsStore Class](../vs140/CSettingsStore-Class.md).  
  
## Return Value  
 `TRUE` if successful; `FALSE` if the class identified by `pRTI` is not derived from `CSettingsStore`.  
  
## Remarks  
 You can use the [CSettingsStoreSP Class](../vs140/CSettingsStoreSP-Class.md) to derive classes from `CSettingsStore`. Use the method `SetRuntimeClass` if you want to create objects of a custom class that is derived from `CSettingsStore`.  
  
## Requirements  
 **Header:** afxsettingsstore.h  
  
## See Also  
 [CSettingsStoreSP Class](../vs140/CSettingsStoreSP-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CSettingsStore Class](../vs140/CSettingsStore-Class.md)   
 [CSettingsStoreSP::Create](../vs140/CSettingsStoreSP--Create.md)