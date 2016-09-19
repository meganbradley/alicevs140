---
title: "CParabolicTransitionFromAcceleration Class"
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
ms.assetid: 1e59b86f-358b-4da0-a4fd-8eaf5e85e00f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CParabolicTransitionFromAcceleration Class
Encapsulates a parabolic-acceleration transition.  
  
## Syntax  
  
```  
class CParabolicTransitionFromAcceleration : public CBaseTransition;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CParabolicTransitionFromAcceleration::CParabolicTransitionFromAcceleration](#cparabolictransitionfromacceleration__cparabolictransitionfromacceleration)|Constructs a parabolic-acceleration transition and initializes it with specified parameters.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CParabolicTransitionFromAcceleration::Create](#cparabolictransitionfromacceleration__create)|Calls the transition library to create encapsulated transition COM object. (Overrides [CBaseTransition::Create](../vs140/CBaseTransition-Class.md#cbasetransition__create).)|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CParabolicTransitionFromAcceleration::m_dblAcceleration](#cparabolictransitionfromacceleration__m_dblacceleration)|The acceleration of the animation variable during the transition.|  
|[CParabolicTransitionFromAcceleration::m_dblFinalValue](#cparabolictransitionfromacceleration__m_dblfinalvalue)|The value of the animation variable at the end of the transition.|  
|[CParabolicTransitionFromAcceleration::m_dblFinalVelocity](#cparabolictransitionfromacceleration__m_dblfinalvelocity)|The velocity of the animation variable at the end of the transition.|  
  
## Remarks  
 During a parabolic-acceleration transition, the value of the animation variable changes from the initial value to the final value ending at a specified velocity. You can control how quickly the variable reaches the final value by specifying the rate of acceleration. Because all transitions are cleared automatically, it's recommended to allocated them using operator new. The encapsulated IUIAnimationTransition COM object is created by CAnimationController::AnimateGroup, until then it's NULL. Changing member variables after creation of this COM object has no effect.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CBaseTransition](../vs140/CBaseTransition-Class.md)  
  
 [CParabolicTransitionFromAcceleration](../vs140/CParabolicTransitionFromAcceleration-Class.md)  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
##  <a name="cparabolictransitionfromacceleration__cparabolictransitionfromacceleration"></a>  CParabolicTransitionFromAcceleration::CParabolicTransitionFromAcceleration  
 Constructs a parabolic-acceleration transition and initializes it with specified parameters.  
  
```  
CParabolicTransitionFromAcceleration(  
   DOUBLE dblFinalValue,  
   DOUBLE dblFinalVelocity,  
   DOUBLE dblAcceleration  
);  
```  
  
### Parameters  
 `dblFinalValue`  
 The value of the animation variable at the end of the transition.  
  
 `dblFinalVelocity`  
 The velocity of the animation variable at the end of the transition.  
  
 `dblAcceleration`  
 The acceleration of the animation variable during the transition.  
  
##  <a name="cparabolictransitionfromacceleration__create"></a>  CParabolicTransitionFromAcceleration::Create  
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
  
##  <a name="cparabolictransitionfromacceleration__m_dblacceleration"></a>  CParabolicTransitionFromAcceleration::m_dblAcceleration  
 The acceleration of the animation variable during the transition.  
  
```  
DOUBLE m_dblAcceleration;  
```  
  
##  <a name="cparabolictransitionfromacceleration__m_dblfinalvalue"></a>  CParabolicTransitionFromAcceleration::m_dblFinalValue  
 The value of the animation variable at the end of the transition.  
  
```  
DOUBLE m_dblFinalValue;  
```  
  
##  <a name="cparabolictransitionfromacceleration__m_dblfinalvelocity"></a>  CParabolicTransitionFromAcceleration::m_dblFinalVelocity  
 The velocity of the animation variable at the end of the transition.  
  
```  
DOUBLE m_dblFinalVelocity;  
```  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)