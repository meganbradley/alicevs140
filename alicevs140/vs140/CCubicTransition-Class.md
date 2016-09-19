---
title: "CCubicTransition Class"
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
ms.assetid: 4fc30e9c-160c-45e1-bdbe-51adf8fee9c5
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCubicTransition Class
Encapsulates a cubic transition.  
  
## Syntax  
  
```  
class CCubicTransition : public CBaseTransition;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CCubicTransition::CCubicTransition](#ccubictransition__ccubictransition)|Constructs a transition object and initializes its parameters.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CCubicTransition::Create](#ccubictransition__create)|Calls the transition library to create encapsulated transition COM object. (Overrides [CBaseTransition::Create](../vs140/CBaseTransition-Class.md#cbasetransition__create).)|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CCubicTransition::m_dblFinalValue](#ccubictransition__m_dblfinalvalue)|The value of the animation variable at the end of the transition.|  
|[CCubicTransition::m_dblFinalVelocity](#ccubictransition__m_dblfinalvelocity)|The velocity of the variable at the end of the transition.|  
|[CCubicTransition::m_duration](#ccubictransition__m_duration)|The duration of the transition.|  
  
## Remarks  
 During a cubic transition, the value of the animation variable changes from its initial value to a specified final value over the duration of the transition, ending at a specified velocity. Because all transitions are cleared automatically, it's recommended to allocated them using operator new. The encapsulated IUIAnimationTransition COM object is created by CAnimationController::AnimateGroup, until then it's NULL. Changing member variables after creation of this COM object has no effect.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CBaseTransition](../vs140/CBaseTransition-Class.md)  
  
 [CCubicTransition](../vs140/CCubicTransition-Class.md)  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
##  <a name="ccubictransition__ccubictransition"></a>  CCubicTransition::CCubicTransition  
 Constructs a transition object and initializes its parameters.  
  
```  
CCubicTransition(  
   UI_ANIMATION_SECONDS duration,  
   DOUBLE finalValue,  
   DOUBLE finalVelocity  
);  
```  
  
### Parameters  
 `duration`  
 The duration of the transition.  
  
 `finalValue`  
 The value of the animation variable at the end of the transition.  
  
 `finalVelocity`  
 The velocity of the variable at the end of the transition.  
  
##  <a name="ccubictransition__create"></a>  CCubicTransition::Create  
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
  
##  <a name="ccubictransition__m_dblfinalvalue"></a>  CCubicTransition::m_dblFinalValue  
 The value of the animation variable at the end of the transition.  
  
```  
DOUBLE m_dblFinalValue;  
```  
  
##  <a name="ccubictransition__m_dblfinalvelocity"></a>  CCubicTransition::m_dblFinalVelocity  
 The velocity of the variable at the end of the transition.  
  
```  
DOUBLE m_dblFinalVelocity;  
```  
  
##  <a name="ccubictransition__m_duration"></a>  CCubicTransition::m_duration  
 The duration of the transition.  
  
```  
UI_ANIMATION_SECONDS m_duration;  
```  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)