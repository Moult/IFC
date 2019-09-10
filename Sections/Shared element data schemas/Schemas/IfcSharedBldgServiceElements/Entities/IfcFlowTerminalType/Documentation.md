﻿The element type _IfcFlowTerminalType_ defines a list of commonly shared property set definitions of a flow terminal and an optional set of product representations. It is used to define a flow terminal specification (i.e. the specific product information, that is common to all occurrences of that product type).

> <font size="-1">
		NOTE: The product representations are defined as
		representation maps (at the level of the supertype <i>IfcTypeProduct</i>, which
		get assigned by an element occurrence instance through the
		<i>IfcShapeRepresentation.Item[1]</i> being an
		<i>IfcMappedItem</i>.
    	</font>

A flow terminal type is used to define the common properties of a flow terminal that may be applied to many occurrences of that type. A flow terminal acts as a terminus or beginning element in a distribution system such as a ceiling register in a ducted air distribution system, a sink in a waste-water system, or a light fixture in an electrical lighting system. Flow terminal types (or the instantiable subtypes) may be exchanged without being already assigned to occurrences.

The occurrences of the _IfcFlowTerminalType_ are represented by instances of _IfcFlowTerminal_ or its subtypes.

> <font color="#0000ff" size="-1">
    	HISTORY: New entity in IFC Release 2x2.<br>
    	</font>