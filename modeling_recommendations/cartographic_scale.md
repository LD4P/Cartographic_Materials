Cartographic Scale Recommendations
======================
Linked Data for Production -- Cartographic Materials Working Group   
June 2018

**Table of Contents**
> - [Overview](#overview)
> - [Relevant Documentation](#documentation)
> - [Summary of Recommendations](#recommendations)
> - [BIBFRAME Approach to Scale](#bibframe)
> - [GCRO Approach to Scale](#recommended_approach)
> - [Side-by-side rdf examples](#examples)
> - [Discussion/Future Work](#future-work)

<a name="overview">Overview</a>
---------


<a name="documentation">Relevant Documentation</a>
------------------------


<a name="recommendations">Summary of Recommendations</a>
---------------------------


-   Define the following new classes:
> - gcro:HorizontalScale
> - gcro:VerticalScale
> - gcro:ScaleIndeterminable
> - gcro:ScaleNotDetermined
> - gcro:NotDrawnToScale
> - gcro:ScaleVaries
> - gcro:ScaleNotGiven
> - gcro:ScalesDiffer
> - gcro:ScaleAccuracy  
> > with new Named Individuals:   
> > - grco:ExplicitScale  
> > - grco:ApproximateScale  
> > - gcro:InaccurateScale  
> > - gcro:ScaleAccuracyUnknown  
> - gcro:ScaleSource   
> > with new Named Individuals:   
> > - grco:RepresentativeFraction  
> > - gcro:VerbalStatement  
> > - gcro:ScaleBar  
> > - gcro:CalculatedFromPrimarySource  
> > - gcro:DerivedOther

-   Define the following new properties:
> - gcro:scaleAccuracy
> - gcro:scaleSource
> - gcro:representativeFractionDenominator

<a name="bibframe">BIBFRAME Approach to Scale</a>
---------------------------------

### Model Diagram

### Involved Classes

### Involved Properties


<a name="recommended_approach">LD4P-CM Recommended Approach to Scale</a>
------------------------------------
### Model Diagram

![Diagram](/modeling_recommendations/modeling_diagrams/Scale.png)

### Involved Classes

**bf:Scale**
> - **Label**: Scale
> - **URI:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** 	Ratio of the dimensions of a form contained or embodied in a resource to the dimensions of the entity it represents, e.g., for images or cartographic resources.

**gcro:HorizontalScale**
> - **Label**: Horizontal scale
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** 	The ratio of distances on a map to the corresponding horizontal distance in nature (Ency. Dict. of Cart.).

**gcro:VerticalScale**
> - **Label**: Vertical scale
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** 	The ratio of vertical distances on Profiles, Sections, Block Diagrams or three-dimensional representations to the corresponding distances in nature (Ency. Dict. of Cart.).

**gcro:ScaleIndeterminable**
> - **Label**: Scale indeterminable
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** 	Used to describe a cartographic resource when an effort to determine the scale of a resource is impossible, for example, when there is a bar scale but no units of measurement are given (Cartographic Resources Manual).

**gcro:ScaleNotDetermined**
> - **Label**: Scale not determined
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** 	Use when scale is represented verbally or graphically in the material, but cannot be expressed as a representative fraction, e.g., because of lack of legibility or with unfamiliar units of measure (DCRM-C).

**gcro:NotDrawnToScale**
> - **Label**: Not drawn to scale
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** Used to describe a cartographic resource when it is not drawn to scale.

**gcro:ScaleVaries**
> - **Label**: Scale varies
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** A scale designation for a resource whose scale is variable across the resource, when the range of values cannot be determined (RDA). Used to describe one map/diagram/plan, etc. that is drawn on a variable scale.

**gcro:ScaleNotGiven**
> - **Label**: Scale not given
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** 	
If no scale is found in the material (whether as a representative fraction, verbally, or graphically), give the statement "Scale not given" (DCRM-C).

**gcro:ScalesDiffer**
> - **Label**: Scales differ
> - **URI:** tbd
> - **SubclassOf:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Definition:** Used to describe a cartographic resource in which the main maps, etc., are of more than one scale (Adapted from Cartographic Resources Manual).

### Named Individuals

### Involved Properties

**bf:scale** (Object property)
> - **Label**: Scale
> - **URI:** http://id.loc.gov/ontologies/bibframe/scale
> - **Definition:** Ratio of the dimensions of a form contained or embodied in a resource to the dimensions of the entity it represents, e.g., for images or cartographic resources.
> - **Domain:** Unspecified
> - **Range:** http://id.loc.gov/ontologies/bibframe/Scale

**gcro:scaleAccuracy** (Object property)
> - **Label**: Has Scale Accuracy
> - **URI:** tbd
> - **Definition:** Accuracy of the scale statement.
> - **Domain:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Range:** gcro:ScaleAccuracy

**gcro:scaleSource** (Object property)
> - **Label**: Has Scale Source
> - **URI:** tbd
> - **Definition:** Has Scale Source.
> - **Domain:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Range:** gcro:ScaleSource

**gcro:representativeFractionDenominator** (Data property)
> - **Label**: Representative Fraction Denominator
> - **URI:** tbd
> - **Definition:** The denominator of the scale's representative fraction.
> - **Domain:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Range:** http://www.w3.org/2000/01/rdf-schema#Literal
> - **Note:** Representative Fraction Denominator value should take form of xsd:integer datatype

**rdau:P60510** (Data property)
> - **Label**: has additional scale information
> - **URI:** tbd
> - **Definition:** Relates a resource to an indication of supplemental information about scale.
> - **Domain:** http://id.loc.gov/ontologies/bibframe/Scale
> - **Range:** http://www.w3.org/2000/01/rdf-schema#Literal
> - **Note:** Value should be text literal



<a name="examples">Side-by-side rdf examples</a>
---------------------


<a name="future-work">Discussion/Future Work</a>
----------------------
