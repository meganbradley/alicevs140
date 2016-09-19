---
title: "Standard Dialog Data Validation Routines"
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
ms.assetid: 44dbc222-a897-4949-925e-7660e8964ccd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Standard Dialog Data Validation Routines
This topic lists the standard dialog data validation (DDV) routines used for common MFC dialog controls.  
  
> [!NOTE]
>  The standard dialog data exchange routines are defined in the header file afxdd_.h. However, applications should include afxwin.h.  
  
### DDV Functions  
  
|||  
|-|-|  
|[DDV_MaxChars](../vs140/DDV_MaxChars.md)|Verifies the number of characters in a given control value does not exceed a given maximum.|  
|[DDV_MinMaxByte](../vs140/DDV_MinMaxByte.md)|Verifies a given control value does not exceed a given **BYTE** range.|  
|[DDV_MinMaxDateTime](../vs140/DDV_MinMaxDateTime.md)|Verifies a given control value does not exceed a given time range.|  
|[DDV_MinMaxDouble](../vs140/DDV_MinMaxDouble.md)|Verifies a given control value does not exceed a given **double** range.|  
|[DDV_MinMaxDWord](../vs140/DDV_MinMaxDWord.md)|Verifies a given control value does not exceed a given **DWORD** range.|  
|[DDV_MinMaxFloat](../vs140/DDV_MinMaxFloat.md)|Verifies a given control value does not exceed a given **float** range.|  
|[DDV_MinMaxInt](../vs140/DDV_MinMaxInt.md)|Verifies a given control value does not exceed a given **int** range.|  
|[DDV_MinMaxLong](../vs140/DDV_MinMaxLong.md)|Verifies a given control value does not exceed a given **long** range.|  
|[DDV_MinMaxLongLong](../vs140/DDV_MinMaxLongLong.md)|Verifies a given control value does not exceed a given **LONGLONG** range.|  
|[DDV_MinMaxMonth](../vs140/DDV_MinMaxMonth.md)|Verifies a given control value does not exceed a given date range.|  
|[DDV_MinMaxShort](../vs140/DDV_MinMaxShort.md)|Verifies a given control value does not exceed a given **short** range.|  
|[DDV_MinMaxSlider](../vs140/DDV_MinMaxSlider.md)|Verifies a given slider control value falls within the given range.|  
|[DDV_MinMaxUInt](../vs140/DDV_MinMaxUInt.md)|Verifies a given control value does not exceed a given **UINT** range.|  
|[DDV_MinMaxULongLong](../vs140/DDV_MinMaxULongLong.md)|Verifies a given control value does not exceed a given **ULONGLONG** range.|  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)