﻿**Definition from ISO/CD 10303-42:1992**: A surface of revolution (IfcSurfaceOfRevolution) is the surface obtained by rotating a curve one complete revolution about an axis. The data shall be interpreted as below.

The parameterization is as follows where the curve has a parameterization <font face="Symbol">l</font>(_u_):

> 
>> **C** = AxisPosition.Location  
>> **V** = AxisPosition.Z
>> 
>> ![Image](../../../../../../figures/ifcsurfaceofresolution-math1.gif)
>>


> 
In order to produce a single-value surface the a complete revolution, the curve shall be such that when expressed in a cylindrical coordinate system the curve shall be such that when expressed in a cylindrical coordinate system (_r,&phi; ,z_) centred at C with an axis V no two distinct parametric points on the curve shall have the same values for (_r, z_).

For a surface of revolution the parametric range is 0 &lt; _u_ &lt; 360 degree. The parameterization range for _v_ is defined by referenced curve.

> <font size="-1" color="#0000FF">NOTE: Corresponding STEP entity:
		  surface_of_revolution. Please refer to ISO/IS 10303-42:1994, p.76 for the final
		  definition of the formal standard. </font>
> 
> <font color="#0000FF" size="-1">HISTORY: New entity in IFC Release
		  2x.</font>
>

**Informal propositions**:

1. The surface shall not self-intersect
2. The swept curve shall not be coincident with the axis line for any finite part of its legth.