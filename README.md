# touch-and-go
The interface for 3d manipulation of orthogonal cuboids via 2d finger touches.

### goals
1. allow for simple, intuitive editing
2. welcoming for first-time users
3. satisfying for experienced professionals
4. consistent interface

### strategies
1. focus on orthoganal cubioids
2. edit other volumes based on oriented bounding boxes, with a fixed orientation as you see fit.
3. manipulation logic favors object's geometry over scene orientation or precise finger locations
4. 'snap' to one of relatively few states, assume each input has only limited, high-resolution input, apply as much resolution as possible to the relavant variable.
5. grids and axes can be overlaid, turned on and off for interaction and orientation.  these should probaby off or *minimal* by default

## Touch sequence

|   0   |   1   |   >1   |
|:------|:------|:-------|
|nothing happened yet    |   select object, itinital manipulation   |  pick first, use as 1 |

|   0   |   1   |   1 dragged   |
|:------|:------|:-------|
| abort, deselect  |   still waiting   |  use drag to set primary axis, translate along it |


|   0   |   1   |   1 dragged   |
|:------|:------|:-------|


