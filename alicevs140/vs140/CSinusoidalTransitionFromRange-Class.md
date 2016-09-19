---
title: "CSinusoidalTransitionFromRange Class"
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
ms.assetid: 8b66a729-5f10-431a-b055-e3600d0065da
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSinusoidalTransitionFromRange Class
Encapsulates a sinusoidal-range transition that has a given range of oscillation.  
  
## Syntax  
  
```  
class CSinusoidalTransitionFromRange : public CBaseTransition;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSinusoidalTransitionFromRange::CSinusoidalTransitionFromRange](#csinusoidaltransitionfromrange__csinusoidaltransitionfromrange)|Constructs a transition object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSinusoidalTransitionFromRange::Create](#csinusoidaltransitionfromrange__create)|Calls the transition library to create encapsulated transition COM object. (Overrides [CBaseTransition::Create](../vs140/CBaseTransition-Class.md#cbasetransition__create).)|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CSinusoidalTransitionFromRange::m_dblMaximumValue](#csinusoidaltransitionfromrange__m_dblmaximumvalue)|The value of the animation variable at a peak of the sinusoidal wave.|  
|[CSinusoidalTransitionFromRange::m_dblMinimumValue](#csinusoidaltransitionfromrange__m_dblminimumvalue)|The value of the animation variable at a trough of the sinusoidal wave.|  
|[CSinusoidalTransitionFromRange::m_duration](#csinusoidaltransitionfromrange__m_duration)|The duration of the transition.|  
|[CSinusoidalTransitionFromRange::m_period](#csinusoidaltransitionfromrange__m_period)|The period of oscillation of the sinusoidal wave in seconds.|  
|[CSinusoidalTransitionFromRange::m_slope](#csinusoidaltransitionfromrange__m_slope)|The slope at the start of the transition.|  
  
## Remarks  
 The value of the animation variable fluctuates between the specified minimum and maximum values over the entire duration of a sinusoidal-range transition. The slope parameter is used to disambiguate between the two possible sine waves specified by the other parameters. Because all transitions are cleared automatically, it's recommended to allocated them using operator new. The encapsulated IUIAnimationTransition COM object is created by CAnimationController::AnimateGroup, until then it's NULL. Changing member variables after creation of this COM object has no effect.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CBaseTransition](../vs140/CBaseTransition-Class.md)  
  
 [CSinusoidalTransitionFromRange](../vs140/CSinusoidalTransitionFromRange-Class.md)  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
##  <a name="csinusoidaltransitionfromrange__create"></a>  CSinusoidalTransitionFromRange::Create  
 Calls the transition library to create encapsulated transition COM object.  
  
```  
virtual BOOL Create(  
   IUIAnimationTransitionLibrary* pLibrary,  
   IUIAnimationTransitionFactory* */  
);  
```  
  
### Parameters  
 `pLibrary`  
 A pointer to transition library, which is responsible for creation of standard transitions.  
  
### Return Value  
 TRUE if transition is created successfully; otherwise FALSE.  
  
##  <a name="csinusoidaltransitionfromrange__csinusoidaltransitionfromrange"></a>  CSinusoidalTransitionFromRange::CSinusoidalTransitionFromRange  
 Constructs a transition object.  
  
```  
CSinusoidalTransitionFromRange(  
   UI_ANIMATION_SECONDS duration,  
   DOUBLE dblMinimumValue,  
   DOUBLE dblMaximumValue,  
   UI_ANIMATION_SECONDS period,  
   UI_ANIMATION_SLOPE slope  
);  
```  
  
### Parameters  
 `duration`  
 The duration of the transition.  
  
 `dblMinimumValue`  
 The value of the animation variable at a trough of the sinusoidal wave.  
  
 `dblMaximumValue`  
 The value of the animation variable at a peak of the sinusoidal wave.  
  
 `period`  
 The period of oscillation of the sinusoidal wave in seconds.  
  
 `slope`  
 The slope at the start of the transition.  
  
##  <a name="csinusoidaltransitionfromrange__m_dblmaximumvalue"></a>  CSinusoidalTransitionFromRange::m_dblMaximumValue  
 The value of the animation variable at a peak of the sinusoidal wave.  
  
```  
DOUBLE m_dblMaximumValue;  
```  
  
##  <a name="csinusoidaltransitionfromrange__m_dblminimumvalue"></a>  CSinusoidalTransitionFromRange::m_dblMinimumValue  
 The value of the animation variable at a trough of the sinusoidal wave.  
  
```  
DOUBLE m_dblMinimumValue;  
```  
  
##  <a name="csinusoidaltransitionfromrange__m_duration"></a>  CSinusoidalTransitionFromRange::m_duration  
 The duration of the transition.  
  
```  
UI_ANIMATION_SECONDS m_duration;  
```  
  
##  <a name="csinusoidaltransitionfromrange__m_period"></a>  CSinusoidalTransitionFromRange::m_period  
 The period of oscillation of the sinusoidal wave in seconds.  
  
```  
UI_ANIMATION_SECONDS m_period;  
```  
  
##  <a name="csinusoidaltransitionfromrange__m_slope"></a>  CSinusoidalTransitionFromRange::m_slope  
 The slope at the start of the transition.  
  
```  
UI_ANIMATION_SLOPE m_slope;  
```  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)