---
title: "CSettingsStoreSP::Create"
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
ms.assetid: 63879b65-1724-4241-9402-14e27463525d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSettingsStoreSP::Create
Creates a new instance of an object that is derived from the [CSettingsStore Class](../vs140/CSettingsStore-Class.md).  
  
## Syntax  
  
```  
CSettingsStore& CSettingsStoreSP Create(  
   BOOL bAdmin,  
   BOOL bReadOnly  
);  
```  
  
#### Parameters  
 [in] `bAdmin`  
 A Boolean parameter that determines whether a `CSettingsStore` object is created in administrator mode.  
  
 [in] `bReadOnly`  
 A Boolean parameter that determines whether a `CSettingsStore` object is created for read-only access.  
  
## Return Value  
 A reference to the newly created `CSettingsStore` object.  
  
## Remarks  
 You can use the method [CSettingsStoreSP::SetRuntimeClass](../vs140/CSettingsStoreSP--SetRuntimeClass.md) to determine what type of object `CSettingsStoreSP::Create` will create. By default, this method creates a `CSettingsStore` object.  
  
 If you create a `CSettingsStore` object in administrator mode, the default location for all registry access is HKEY_LOCAL_MACHINE. Otherwise, the default location for all registry access is HKEY_CURRENT_USER.  
  
 If `bAdmin` is `TRUE`, the application must have administration rights. Otherwise, it will fail when it tries to access the registry.  
  
## Example  
 The following example demonstrates how to use the `Create` method of the `CSettingsStoreSP` class.  
  
 [!CODE [NVC_MFC_RibbonApp#33](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#33)]  
  
## Requirements  
 **Header:** afxsettingsstore.h  
  
## See Also  
 [CSettingsStoreSP Class](../vs140/CSettingsStoreSP-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CSettingsStoreSP::SetRuntimeClass](../vs140/CSettingsStoreSP--SetRuntimeClass.md)   
 [CSettingsStore Class](../vs140/CSettingsStore-Class.md)