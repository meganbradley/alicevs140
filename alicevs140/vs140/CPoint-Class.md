---
title: "CPoint Class"
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
ms.assetid: a6d4db93-35cc-444d-9221-c3e160f6edaa
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPoint Class
Similar to the Windows             `POINT` structure.  
  
## Syntax  
  
```  
class CPoint : public tagPOINT  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CPoint::CPoint](#cpoint__cpoint)|Constructs a                                         `CPoint`.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CPoint::Offset](#cpoint__offset)|Adds values to the                                         **x** and                                         **y** members of the                                         `CPoint`.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CPoint::operator -](#cpoint__operator_-)|Returns the difference of a                                         `CPoint` and a size, or the negation of a point, or the size difference between two points, or the offset by a negative size.|  
|[CPoint::operator !=](#cpoint__operator__neq)|Checks for inequality between two points.|  
|[CPoint::operator +](#cpoint__operator__add)|Returns the sum of a                                         `CPoint` and a size or point, or a                                         `CRect` offset by a size.|  
|[CPoint::operator +=](#cpoint__operator__add_eq)|Offsets                                         `CPoint` by adding a size or point.|  
|[CPoint::operator -=](428fb5e0ce0f)|Offsets                                         `CPoint` by subtracting a size or point.|  
|[CPoint::operator ==](#cpoint__operator__eq_eq)|Checks for equality between two points.|  
  
## Remarks  
 It also includes member functions to manipulate                 `CPoint` and                 [POINT](../vs140/POINT-Structure.md) structures.  
  
 A                 `CPoint` object can be used wherever a                 `POINT` structure is used. The operators of this class that interact with a "size" accept either                 [CSize](../vs140/CSize-Class.md) objects or                 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structures, since the two are interchangeable.  
  
> [!NOTE]
>  This class is derived from the                     `tagPOINT` structure. (The name                     `tagPOINT` is a less commonly used name for the                     `POINT` structure.) This means that the data members of the                     `POINT` structure,                     `x` and                     `y`, are accessible data members of                     `CPoint`.  
  
> [!NOTE]
>  For more information on shared utility classes (like                     `CPoint`), see                     [Shared Classes](../vs140/ATL-MFC-Shared-Classes.md).  
  
## Inheritance Hierarchy  
 `tagPOINT`  
  
 `CPoint`  
  
## Requirements  
 **Header:** atltypes.h  
  
##  <a name="cpoint__cpoint"></a>  CPoint::CPoint  
 Constructs a                 `CPoint` object.  
  
```  
CPoint( ) throw( );   
CPoint(  
    int                 initX,  
    int                 initY   
) throw( );  
CPoint(  
    POINT                 initPt   
) throw( );  
CPoint(  
    SIZE                 initSize   
) throw( );  
CPoint(  
    LPARAM                 dwPoint   
) throw( );  
```  
  
### Parameters  
 `initX`  
 Specifies the value of the                                 `x` member of                                 `CPoint`.  
  
 `initY`  
 Specifies the value of the                                 `y` member of                                 `CPoint`.  
  
 `initPt`  
 [POINT](../vs140/POINT-Structure.md) structure or                                 `CPoint` that specifies the values used to initialize                                 `CPoint`.  
  
 `initSize`  
 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or                                 [CSize](../vs140/CSize-Class.md) that specifies the values used to initialize                                 `CPoint`.  
  
 `dwPoint`  
 Sets the                                 `x` member to the low-order word of                                 `dwPoint` and the                                 `y` member to the high-order word of                                 `dwPoint`.  
  
### Remarks  
 If no arguments are given,                         `x` and                         `y` members are set to 0.  
  
### Example  
  
```  
  
CPoint   ptTopLeft(0,0);  
  
// works from a POINT, too  
  
POINT   ptHere;  
ptHere.x = 35;  
ptHere.y = 95;  
  
CPoint   ptMFCHere(ptHere);  
  
// works from A SIZE  
  
SIZE   sHowBig;  
sHowBig.cx = 300;  
sHowBig.cy = 10;  
  
CPoint ptMFCBig(sHowBig);  
  
// or from a DWORD  
  
DWORD   dwSize;  
dwSize = MAKELONG(35, 95);  
  
CPoint ptFromDouble(dwSize);  
ASSERT(ptFromDouble == ptMFCHere);     
```  
  
##  <a name="cpoint__offset"></a>  CPoint::Offset  
 Adds values to the                 **x** and                 **y** members of the                 `CPoint`.  
  
```  
  
void Offset(  
   int   
xOffset  
,  
   int   
yOffset  
) throw( );  
void Offset(  
   POINT   
point  
) throw( );  
void Offset(  
   SIZE   
size  
) throw( );  
  
```  
  
### Parameters  
 *xOffset*  
 Specifies the amount to offset the                                 **x** member of the                                 `CPoint`.  
  
 *yOffset*  
 Specifies the amount to offset the                                 **y** member of the                                 `CPoint`.  
  
 `point`  
 Specifies the amount (                                [POINT](../vs140/POINT-Structure.md) or                                 `CPoint`) to offset the                                 `CPoint`.  
  
 `size`  
 Specifies the amount (                                [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) or                                 [CSize](../vs140/CSize-Class.md)) to offset the                                 `CPoint`.  
  
### Example  
 [!CODE [NVC_ATLMFC_Utilities#28](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#28)]  
  
##  <a name="cpoint__operator__eq_eq"></a>  CPoint::operator ==  
 Checks for equality between two points.  
  
```  
  
BOOL operator ==(  
   POINT   
point  
) const throw( );  
  
```  
  
### Parameters  
 `point`  
 Contains a                                 [POINT](../vs140/POINT-Structure.md) structure or                                 `CPoint` object.  
  
### Return Value  
 Nonzero if the points are equal; otherwise 0.  
  
### Example  
 [!CODE [NVC_ATLMFC_Utilities#29](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#29)]  
  
##  <a name="cpoint__operator__neq"></a>  CPoint::operator !=  
 Checks for inequality between two points.  
  
```  
  
BOOL operator!=(  
   POINT   
point  
) const throw( );  
  
```  
  
### Parameters  
 `point`  
 Contains a                                 [POINT](../vs140/POINT-Structure.md) structure or                                 `CPoint` object.  
  
### Return Value  
 Nonzero if the points are not equal; otherwise 0.  
  
### Example  
 [!CODE [NVC_ATLMFC_Utilities#30](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#30)]  
  
##  <a name="cpoint__operator__add_eq"></a>  CPoint::operator +=  
 The first overload adds a size to the                 `CPoint`.  
  
```  
  
void operator +=(  
   SIZE   
size  
) throw( );  
void operator +=(  
   POINT   
point  
) throw( );  
  
```  
  
### Parameters  
 `size`  
 Contains a                                 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or                                 [CSize](../vs140/CSize-Class.md) object.  
  
 `point`  
 Contains a                                 [POINT](../vs140/POINT-Structure.md) structure or                                 [CPoint](../vs140/CPoint-Class.md) object.  
  
### Remarks  
 The second overload adds a point to the                         `CPoint`.  
  
 In both cases, addition is done by adding the                         **x** (or                         **cx**) member of the right-hand operand to the                         **x** member of the                         `CPoint` and adding the                         **y** (or                         **cy**) member of the right-hand operand to the                         **y** member of the                         `CPoint`.  
  
 For example, adding                         `CPoint(5, -7)` to a variable which contains                         `CPoint(30, 40)` changes the variable to                         `CPoint(35, 33)`.  
  
### Example  
 [!CODE [NVC_ATLMFC_Utilities#31](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#31)]  
  
##  <a name="cpoint__operator_-_eq"></a>  CPoint::operator -=  
 The first overload subtracts a size from the                 `CPoint`.  
  
```  
  
void operator -=(  
   SIZE   
size  
) throw( );  
void operator -=(  
   POINT   
point  
) throw( );  
  
```  
  
### Parameters  
 `size`  
 Contains a                                 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or                                 [CSize](../vs140/CSize-Class.md) object.  
  
 `point`  
 Contains a                                 [POINT](../vs140/POINT-Structure.md) structure or                                 [CPoint](../vs140/CPoint-Class.md) object.  
  
### Remarks  
 The second overload subtracts a point from the                         `CPoint`.  
  
 In both cases, subtraction is done by subtracting the                         **x** (or                         **cx**) member of the right-hand operand from the                         **x** member of the                         `CPoint` and subtracting the                         **y** (or                         **cy**) member of the right-hand operand from the                         **y** member of the                         `CPoint`.  
  
 For example, subtracting                         `CPoint(5, -7)` from a variable which contains                         `CPoint(30, 40)` changes the variable to                         `CPoint(25, 47)`.  
  
### Example  
 [!CODE [NVC_ATLMFC_Utilities#32](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#32)]  
  
##  <a name="cpoint__operator__add"></a>  CPoint::operator +  
 Use this operator to offset                 `CPoint` by a                 `CPoint` or                 `CSize` object, or to offset a                 `CRect` by a                 `CPoint`.  
  
```  
  
CPoint operator +(  
   SIZE   
size  
) const throw( );  
CPoint operator +(  
   POINT   
point  
) const throw( );  
CRect operator +(  
   const RECT*   
lpRect  
) const throw( );  
  
```  
  
### Parameters  
 `size`  
 Contains a                                 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or                                 [CSize](../vs140/CSize-Class.md) object.  
  
 `point`  
 Contains a                                 [POINT](../vs140/POINT-Structure.md) structure or                                 [CPoint](../vs140/CPoint-Class.md) object.  
  
 `lpRect`  
 Contains a pointer to a                                 [RECT](../vs140/RECT-Structure.md) structure or                                 [CRect](../vs140/CRect-Class.md) object.  
  
### Return Value  
 A                         `CPoint` that is offset by a size, a                         **CPoint** that is offset by a point, or a                         **CRect** offset by a point.  
  
### Remarks  
 For example, using one of the first two overloads to offset the point                         `CPoint(25, -19)` by a point                         `CPoint(15, 5)` or size                         `CSize(15, 5)` returns the value                         `CPoint(40, -14)`.  
  
 Adding a rectangle to a point returns the rectangle after being offset by the                         **x** and                         **y** values specified in the point. For example, using the last overload to offset a rectangle                         `CRect(125, 219, 325, 419)` by a point                         `CPoint(25, -19)` returns                         `CRect(150, 200, 350, 400)`.  
  
### Example  
 [!CODE [NVC_ATLMFC_Utilities#33](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#33)]  
  
##  <a name="cpoint__operator_-"></a>  CPoint::operator -  
 Use one of the first two overloads to subtract a                 `CPoint` or                 `CSize` object from                 `CPoint`.  
  
```  
  
CSize operator -(  
   POINT   
point  
) const throw( );  
CPoint operator -(  
   SIZE   
size  
) const throw( );  
CRect operator -(  
   const RECT*   
lpRect  
) const throw( );  
CPoint operator -( ) const throw( );  
  
```  
  
### Parameters  
 `point`  
 A                                 [POINT](../vs140/POINT-Structure.md) structure or                                 [CPoint](../vs140/CPoint-Class.md) object.  
  
 `size`  
 A                                 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or                                 [CSize](../vs140/CSize-Class.md) object.  
  
 `lpRect`  
 A pointer to a                                 [RECT](../vs140/RECT-Structure.md) structure or a                                 [CRect](../vs140/CRect-Class.md) object.  
  
### Return Value  
 A                         `CSize` that is the difference between two points, a                         `CPoint` that is offset by the negation of a size, a                         `CRect` that is offset by the negation of a point, or a                         `CPoint` that is the negation of a point.  
  
### Remarks  
 The third overload offsets a                         `CRect` by the negation of                         `CPoint`. Finally, use the unary operator to negate                         `CPoint`.  
  
 For example, using the first overload to find the difference between two points                         `CPoint(25, -19)` and                         `CPoint(15, 5)` returns                         `CSize(10, -24)`.  
  
 Subtracting a                         `CSize` from                         `CPoint` does the same calculation as above but returns a                         `CPoint` object, not a                         `CSize` object. For example, using the second overload to find the difference between the point                         `CPoint(25, -19)` and the size                         `CSize(15, 5)` returns                         `CPoint(10, -24)`.  
  
 Subtracting a rectangle from a point returns the rectangle offset by the negatives of the                         **x** and                         **y** values specified in the point. For example, using the last overload to offset the rectangle                         `CRect(125, 200, 325, 400)` by the point                         `CPoint(25, -19)` returns                         `CRect(100, 219, 300, 419)`.  
  
 Use the unary operator to negate a point. For example, using the unary operator with the point                         `CPoint(25, -19)` returns                         `CPoint(-25, 19)`.  
  
### Example  
 [!CODE [NVC_ATLMFC_Utilities#34](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#34)]  
  
## See Also  
 [MFC Sample MDI](../vs140/Visual-C---Samples.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [POINT Structure](../vs140/POINT-Structure.md)   
 [CRect](../vs140/CRect-Class.md)   
 [CSize](../vs140/CSize-Class.md)