---
title: "Simple Data Type Classes"
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
ms.assetid: 0d591d68-0a33-49e9-8a6d-90c90de5c16a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Simple Data Type Classes
The following classes encapsulate drawing coordinates, character strings, and time and date information, allowing convenient use of C++ syntax. These objects are used widely as parameters to the member functions of Windows classes in the class library. Because `CPoint`, `CSize`, and `CRect` correspond to the **POINT**, **SIZE**, and `RECT` structures, respectively, in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)], you can use objects of these C++ classes wherever you can use these C-language structures. The classes provide useful interfaces through their member functions. `CStringT` provides very flexible dynamic character strings. `CTime`, `COleDateTime`, `CTimeSpan`, and **COleTimeSpan** represent time and date values. For more information about these classes, see the article [Date and Time](../vs140/Date-and-Time.md).  
  
 The classes that begin with "**COle**" are encapsulations of data types provided by OLE. These data types can be used in Windows programs regardless of whether other OLE features are used.  
  
 [CStringT Class](../vs140/CStringT-Class.md)  
 Holds character strings.  
  
 [CTime](../Topic/CTime%20Class.md)  
 Holds absolute time and date values.  
  
 [COleDateTime](../vs140/COleDateTime-Class.md)  
 Wrapper for the OLE automation type **DATE**. Represents date and time values.  
  
 [CTimeSpan](../vs140/CTimeSpan-Class.md)  
 Holds relative time and date values.  
  
 [COleDateTimeSpan](../vs140/COleDateTimeSpan-Class.md)  
 Holds relative `COleDateTime` values, such as the difference between two `COleDateTime` values.  
  
 [CPoint](../vs140/CPoint-Class.md)  
 Holds coordinate (x, y) pairs.  
  
 [CSize](../vs140/CSize-Class.md)  
 Holds distance, relative positions, or paired values.  
  
 [CRect](../vs140/CRect-Class.md)  
 Holds coordinates of rectangular areas.  
  
 [CImageList](../vs140/CImageList-Class.md)  
 Provides the functionality of the Windows image list. Image lists are used with list controls and tree controls. They can also be used to store and archive a set of same-sized bitmaps.  
  
 [COleVariant](../vs140/COleVariant-Class.md)  
 Wrapper for the OLE automation type **VARIANT**. Data in **VARIANT**s can be stored in many formats.  
  
 [COleCurrency](../vs140/COleCurrency-Class.md)  
 Wrapper for the OLE automation type **CURRENCY**, a fixed-point arithmetic type, with 15 digits before the decimal point and 4 digits after.  
  
> [!NOTE]
>  Beginning with Visual C++ .NET, `CRect`, `CSize`, and `CPoint` have been modified to be usable in either ATL or MFC applications. In addition, `CStringT` has been added to provide an MFC-independent `CString`-like class. For more information on shared utility classes, see [Shared Classes](../vs140/ATL-MFC-Shared-Classes.md).  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)