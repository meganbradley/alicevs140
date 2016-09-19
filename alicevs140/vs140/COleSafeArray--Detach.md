---
title: "COleSafeArray::Detach"
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
ms.assetid: eb061d94-f251-4995-a933-b56d34693d88
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::Detach
Detaches the **VARIANT** data from the `COleSafeArray` object.  
  
## Syntax  
  
```  
  
VARIANT Detach( );  
```  
  
## Return Value  
 The underlying **VARIANT** value in the `COleSafeArray` object.  
  
## Remarks  
 The function detaches the data in a safe array by setting the [VARTYPE](assetId:///317b911b-1805-402d-a9cb-159546bc88b4) of the object to `VT_EMPTY`. It is the caller's responsibility to free the array by calling the Windows function [VariantClear](assetId:///28741d81-8404-4f85-95d3-5c209ec13835).  
  
 On error, the function throws a [COleException](../vs140/COleException-Class.md).  
  
## Example  
 See the example for [COleSafeArray::PutElement](../vs140/COleSafeArray--PutElement.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::Attach](../vs140/COleSafeArray--Attach.md)   
 [VariantClear](assetId:///28741d81-8404-4f85-95d3-5c209ec13835)