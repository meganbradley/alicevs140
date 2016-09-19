---
title: "Invoking Scripts"
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
ms.assetid: eabd41ee-586b-4266-9e92-5aaad04b73a4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Invoking Scripts
[Using Replaceable Parameters (The Registrar's Preprocessor)](../vs140/Using-Replaceable-Parameters--The-Registrar-s-Preprocessor-.md) discusses replacement maps and mentions the Registrar method **AddReplacement**. The Registrar has eight other methods specific to scripting, and all are described in the following table.  
  
|Method|Syntax/Description|  
|------------|-------------------------|  
|**ResourceRegister**|**HRESULT ResourceRegister( LPCOLESTR**  *resFileName* **, UINT**  `nID` **, LPCOLESTR**  `szType` **);**<br /><br /> Registers the script contained in a module's resource. *resFileName* indicates the UNC path to the module itself. `nID` and `szType` contain the resource's ID and type, respectively.|  
|**ResourceUnregister**|**HRESULT ResourceUnregister( LPCOLESTR**  *resFileName* **, UINT**  `nID` **, LPCOLESTR**  `szType` **);**<br /><br /> Unregisters the script contained in a module's resource. *resFileName* indicates the UNC path to the module itself. `nID` and `szType` contain the resource's ID and type, respectively.|  
|**ResourceRegisterSz**|**HRESULT ResourceRegisterSz( LPCOLESTR**  *resFileName* **, LPCOLESTR**  *szID* **, LPCOLESTR**  `szType` **);**<br /><br /> Registers the script contained in a module's resource. *resFileName* indicates the UNC path to the module itself. *szID* and `szType` contain the resource's string identifier and type, respectively.|  
|**ResourceUnregisterSz**|**HRESULT ResourceUnregisterSz( LPCOLESTR**  *resFileName* **, LPCOLESTR**  *szID* **, LPCOLESTR**  `szType` **);**<br /><br /> Unregisters the script contained in a module's resource. *resFileName* indicates the UNC path to the module itself. *szID* and `szType` contain the resource's string identifier and type, respectively.|  
|**FileRegister**|**HRESULT FileRegister( LPCOLESTR**  *fileName*  **);**<br /><br /> Registers the script in a file. *fileName* is a UNC path to a file that contains (or is) a resource script.|  
|**FileUnregister**|**HRESULT FileUnregister( LPCOLESTR**  *fileName*  **);**<br /><br /> Unregisters the script in a file. *fileName* is a UNC path to a file that contains (or is) a resource script.|  
|**StringRegister**|**HRESULT StringRegister( LPCOLESTR**  *data*  **);**<br /><br /> Registers the script in a string. *data* contains the script itself.|  
|**StringUnregister**|**HRESULT StringUnregister( LPCOLESTR**  *data*  **);**<br /><br /> Unregisters the script in a string. *data* contains the script itself.|  
  
 **ResourceRegisterSz** and **ResourceUnregisterSz**, are similar to **ResourceRegister** and **ResourceUnregister**, but allow you to specify a string identifier.  
  
 The methods **FileRegister** and **FileUnregister** are useful if you do not want the script in a resource or if you want the script in its own file. The methods **StringRegister** and **StringUnregister** allow the .rgs file to be stored in a dynamically allocated string.  
  
## See Also  
 [Creating Registrar Scripts](../vs140/Creating-Registrar-Scripts.md)