﻿An _IfcTaskType_ defines a particular type of task that may be specified for use within a work control.

> HISTORY&nbsp; New entity in IFC4

An _IfcTaskType_ provides for all forms of types of task that may be specified. It is a reference definition for a unit of work that may be broken down into (a sequence of) subtasks. Please note that a reference definition can not be part of a workflow definition, i.e. _IfcTaskType_ instances define the most abstract level of a reference process without dependencies to other reference processes.

Usage of _IfcTaskType_ defines the parameters for one or more occurrences of _IfcTask_. Parameters may be specified through property sets that may be enumerated in the _IfcTaskTypeEnum_ data type or through explict attributes of _IfcTaskType_. Task occurrences (_IfcTask_ entities) are linked to the task type through the _IfcRelDefinesByType_ relationship.

Figure 1 shows the definition of a task type that is part of a task template library. Please note that in this example the task type is further subdivided into tasks that define task times (for example, duration) and/or a task sequence.

!["task type instantiation diagram"](../../../../../../figures/ifctasktype_instantiation_diagram.png "Figure 1 &mdash; Task type relationships")

___
## Common Use Definitions
The following concepts are inherited at supertypes:

* _IfcRoot_: [Identity](../../templates/identity.htm), [Revision Control](../../templates/revision-control.htm)

[![Image](../../../img/diagram.png)&nbsp;Instance diagram](../../../annex/annex-d/common-use-definitions/ifctasktype.htm)

{ .use-head}
Object Nesting

The [Object Nesting](../../templates/object-nesting.htm) concept applies to this entity.

_IfcTaskType_ may nest other _IfcTaskType_ or _IfcTask_ entities using the _IfcRelNests_ relationship. Such nesting indicates decomposed level of detail. Nesting of _IfcTask_ entities is used if a task type shall be detailed by a sequence of tasks or if there is a need to include additional time information such as the duration of subtasks. Please note that _IfcTask_ entities being contained within an _IfcTaskType_ are linked with their task occurrences via _IfcRelDefinesByObject_ relationships. It is also possible to define a task type for these _IfcTask_ entities via _IfcRelDefinesByType_ relationships. For further information please see the documentation of _IfcRelDefinesByObject_.