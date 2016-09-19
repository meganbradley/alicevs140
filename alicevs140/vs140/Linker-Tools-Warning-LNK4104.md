---
title: "Linker Tools Warning LNK4104"
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
ms.topic: error-reference
ms.assetid: ca6728db-d616-419a-a570-65e8445c6079
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4104
export of symbol 'symbol' should be PRIVATE  
  
 The `symbol` can be one of the following:  
  
-   `DllCanUnloadNow`  
  
-   `DllGetClassObject`  
  
-   `DllGetClassFactoryFromClassString`  
  
-   `DllGetDocumentation`  
  
-   `DllInitialize`  
  
-   `DllInstall`  
  
-   `DllRegisterServer`  
  
-   `DllRegisterServerEx`  
  
-   `DllRegisterServerExW`  
  
-   `DllUnload`  
  
-   `DllUnregisterServer`  
  
-   `RasCustomDeleteEntryNotify`  
  
-   `RasCustomDial`  
  
-   `RasCustomDialDlg`  
  
-   `RasCustomEntryDlg`  
  
 This warning is emitted when you are building an import library for a DLL and export one of the above functions without specifying it as PRIVATE in the module-definition file. In general, these functions are exported for use only by OLE. Placing them in the import library can lead to unusual behavior when a program linked to the library incorrectly makes calls to them. For more information about the PRIVATE keyword, see [EXPORTS](../vs140/EXPORTS.md).