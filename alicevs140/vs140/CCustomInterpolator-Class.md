---
title: "CCustomInterpolator Class"
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
ms.assetid: 28d85595-989a-40a3-b003-e0e38437a94d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCustomInterpolator Class
Implements a basic interpolator.  
  
## Syntax  
  
```  
class CCustomInterpolator;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CCustomInterpolator::CCustomInterpolator](#ccustominterpolator__ccustominterpolator)|Overloaded. Constructs a custom interpolator object and initializes duration and velocity to specified values.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CCustomInterpolator::GetDependencies](#ccustominterpolator__getdependencies)|Gets the interpolator's dependencies.|  
|[CCustomInterpolator::GetDuration](#ccustominterpolator__getduration)|Gets the interpolator's duration.|  
|[CCustomInterpolator::GetFinalValue](#ccustominterpolator__getfinalvalue)|Gets the final value to which the interpolator leads.|  
|[CCustomInterpolator::Init](#ccustominterpolator__init)|Initializes duration and final value.|  
|[CCustomInterpolator::InterpolateValue](#ccustominterpolator__interpolatevalue)|Interpolates the value at a given offset.|  
|[CCustomInterpolator::InterpolateVelocity](#ccustominterpolator__interpolatevelocity)|Interpolates the velocity at a given offset|  
|[CCustomInterpolator::SetDuration](#ccustominterpolator__setduration)|Sets the interpolator's duration.|  
|[CCustomInterpolator::SetInitialValueAndVelocity](#ccustominterpolator__setinitialvalueandvelocity)|Sets the interpolator's initial value and velocity.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CCustomInterpolator::m_currentValue](#ccustominterpolator__m_currentvalue)|The interpolated value.|  
|[CCustomInterpolator::m_currentVelocity](#ccustominterpolator__m_currentvelocity)|The interpolated velocity.|  
|[CCustomInterpolator::m_duration](#ccustominterpolator__m_duration)|The duration of the transition.|  
|[CCustomInterpolator::m_finalValue](#ccustominterpolator__m_finalvalue)|The final value of a variable at the end of the transition.|  
|[CCustomInterpolator::m_initialValue](#ccustominterpolator__m_initialvalue)|The value of the variable at the start of the transition.|  
|[CCustomInterpolator::m_initialVelocity](#ccustominterpolator__m_initialvelocity)|The velocity of the variable at the start of the transition.|  
  
## Remarks  
 Derive a class from CCustomInterpolator and override all necessary methods in order to implement a custom interpolation algorithm. A pointer to this class should be passed as a parameter to CCustomTransition.  
  
## Inheritance Hierarchy  
 [CCustomInterpolator](../vs140/CCustomInterpolator-Class.md)  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
##  <a name="ccustominterpolator__ccustominterpolator"></a>  CCustomInterpolator::CCustomInterpolator  
 Constructs a custom interpolator object and sets all values to default 0.  
  
```  
CCustomInterpolator();  
CCustomInterpolator(  
   UI_ANIMATION_SECONDS duration,  
   DOUBLE finalValue  
);  
```  
  
### Parameters  
 `duration`  
 The duration of the transition.  
  
 `finalValue`  
  
### Remarks  
 Use CCustomInterpolator::Init to initialize duration and final value later in the code.  
  
##  <a name="ccustominterpolator__getdependencies"></a>  CCustomInterpolator::GetDependencies  
 Gets the interpolator's dependencies.  
  
```  
virtual BOOL GetDependencies(  
   UI_ANIMATION_DEPENDENCIES * initialValueDependencies,  
   UI_ANIMATION_DEPENDENCIES * initialVelocityDependencies,  
   UI_ANIMATION_DEPENDENCIES * durationDependencies  
);  
```  
  
### Parameters  
 `initialValueDependencies`  
 Output. Aspects of the interpolator that depend on the initial value passed to SetInitialValueAndVelocity.  
  
 `initialVelocityDependencies`  
 Output. Aspects of the interpolator that depend on the initial velocity passed to SetInitialValueAndVelocity.  
  
 `durationDependencies`  
 Output. Aspects of the interpolator that depend on the duration passed to SetDuration.  
  
### Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
##  <a name="ccustominterpolator__getduration"></a>  CCustomInterpolator::GetDuration  
 Gets the interpolator's duration.  
  
```  
virtual BOOL GetDuration(  
   UI_ANIMATION_SECONDS * duration  
);  
```  
  
### Parameters  
 `duration`  
 Output. The duration of the transition, in seconds.  
  
### Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
##  <a name="ccustominterpolator__getfinalvalue"></a>  CCustomInterpolator::GetFinalValue  
 Gets the final value to which the interpolator leads.  
  
```  
virtual BOOL GetFinalValue(  
   DOUBLE * value  
);  
```  
  
### Parameters  
 `value`  
 Output. The final value of a variable at the end of the transition.  
  
### Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
##  <a name="ccustominterpolator__init"></a>  CCustomInterpolator::Init  
 Initializes duration and final value.  
  
```  
void Init(  
   UI_ANIMATION_SECONDS duration,  
   DOUBLE finalValue  
);  
```  
  
### Parameters  
 `duration`  
 The duration of the transition.  
  
 `finalValue`  
 The final value of a variable at the end of the transition.  
  
##  <a name="ccustominterpolator__interpolatevalue"></a>  CCustomInterpolator::InterpolateValue  
 Interpolates the value at a given offset.  
  
```  
virtual BOOL InterpolateValue(  
   UI_ANIMATION_SECONDS */,  
   DOUBLE * value  
);  
```  
  
### Parameters  
 `value`  
 Output. The interpolated value.  
  
### Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
##  <a name="ccustominterpolator__interpolatevelocity"></a>  CCustomInterpolator::InterpolateVelocity  
 Interpolates the velocity at a given offset  
  
```  
virtual BOOL InterpolateVelocity(  
   UI_ANIMATION_SECONDS */,  
   DOUBLE * velocity  
);  
```  
  
### Parameters  
 `velocity`  
 Output. The velocity of the variable at the offset.  
  
### Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
##  <a name="ccustominterpolator__m_currentvalue"></a>  CCustomInterpolator::m_currentValue  
 The interpolated value.  
  
```  
DOUBLE m_currentValue;  
```  
  
##  <a name="ccustominterpolator__m_currentvelocity"></a>  CCustomInterpolator::m_currentVelocity  
 The interpolated velocity.  
  
```  
DOUBLE m_currentVelocity;  
```  
  
##  <a name="ccustominterpolator__m_duration"></a>  CCustomInterpolator::m_duration  
 The duration of the transition.  
  
```  
UI_ANIMATION_SECONDS m_duration;  
```  
  
##  <a name="ccustominterpolator__m_finalvalue"></a>  CCustomInterpolator::m_finalValue  
 The final value of a variable at the end of the transition.  
  
```  
DOUBLE m_finalValue;  
```  
  
##  <a name="ccustominterpolator__m_initialvalue"></a>  CCustomInterpolator::m_initialValue  
 The value of the variable at the start of the transition.  
  
```  
DOUBLE m_initialValue;  
```  
  
##  <a name="ccustominterpolator__m_initialvelocity"></a>  CCustomInterpolator::m_initialVelocity  
 The velocity of the variable at the start of the transition.  
  
```  
DOUBLE m_initialVelocity;  
```  
  
##  <a name="ccustominterpolator__setduration"></a>  CCustomInterpolator::SetDuration  
 Sets the interpolator's duration.  
  
```  
virtual BOOL SetDuration(  
   UI_ANIMATION_SECONDS duration  
);  
```  
  
### Parameters  
 `duration`  
 The duration of the transition.  
  
### Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
##  <a name="ccustominterpolator__setinitialvalueandvelocity"></a>  CCustomInterpolator::SetInitialValueAndVelocity  
 Sets the interpolator's initial value and velocity.  
  
```  
virtual BOOL SetInitialValueAndVelocity(  
   DOUBLE initialValue,  
   DOUBLE initialVelocity  
);  
```  
  
### Parameters  
 `initialValue`  
 The value of the variable at the start of the transition.  
  
 `initialVelocity`  
 The velocity of the variable at the start of the transition.  
  
### Return Value  
 The basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)