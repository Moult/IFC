﻿Instances of the entity _IfcStructuralPointAction_ are used to define point actions. Structural loads applicable to point actions are _IfcStructuralLoadSingleForce_ (and subtype), and _IfcStructuralLoadSingleDisplacement_ (and subtype).

The structural load, defining the point action is given by the attribute _AppliedLoad_ at the supertype _IfcStructuralActivity_. The coordinate system, in which the _AppliedLoad_ is defined is given by the attribute _ObjectPlacement_ at the supertype _IfcProduct_.

> <font color="#0000FF" size="-1">HISTORY: New entity in Release IFC2x

		  Edition 2. </font>
> 


****Topology Use Definition****

Special case: If applied to building elements, placement and representation of the structural action are often implied by those of the building elements and are therefore optional for the actions.

Standard case: If applied to structural items, instances of _IfcStructuralPointAction_ shall have a topology representation. It includes a placement and a product representation. The _IfcProductRepresentation_ shall be given by an item of _Representations_ being of type "_IfcTopologyRepresentation_".

**Placement**

The placement for _IfcStructuralPointAction_ is determined at its supertype _IfcProduct_. It is defined by the optional _IfcObjectPlacement_, referenced by _ObjectPlacement_ at _IfcProduct_, which establishes, if given, the object coordinate system that is referenced by the applied load.

* If the _ObjectPlacement_ attribute is omitted, then all topological representations are given directly in world coordinates.
* If the _ObjectPlacement_ attribute is provided, then it establishes an object coordinate system for all topological representations which are given object coordinates. 
    * If the _PlacementRelTo_ relationship of _IfcLocalPlacement_ is omitted, the object coordinate system is established within the world coordinate system.
    * If the _PlacementRelTo_ relationship of _IfcLocalPlacement_ is given, it shall point to the local placement of the same _IfcSpatialStructureElement_, which is used in the _ContainedInStructure_ inverse attribute, or to a spatial structure element at a higher level, referenced by that. 

**Topology Representation**

Instances of _IfcStructuralPointAction_ may have a topology representation given by a vertex with an optional additional geometric representation by a Cartesian point. It can be provided by either

* _IfcVertex_
* _IfcVertexPoint_

which should be the single item of _IfcTopologyRepresentation.Items_. If no topology representation is given, the location of the placement is taken as the vertex at which the point actions acts upon the structural item.