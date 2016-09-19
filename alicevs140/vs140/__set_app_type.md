---
title: "__set_app_type"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - __set_app_type
apilocation: 
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - api-ms-win-crt-runtime-l1-1-0.dll
apitype: DLLExport
ms.assetid: f0ac0f4d-70e6-4e96-9e43-eb9d1515490c
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __set_app_type
Sets the current application type.  
  
## Syntax  
  
```cpp  
void __set_app_type (  
   int at  
   )  
```  
  
#### Parameters  
 `at`  
 A value that indicates the application type. The possible values are:  
  
|Value|Description|  
|-----------|-----------------|  
|_UNKNOWN_APP|Unknown application type.|  
|_CONSOLE_APP|Console (command-line) application.|  
|_GUI_APP|GUI (Windows) application.|  
  
## Remarks  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|__set_app_type|internal.h|