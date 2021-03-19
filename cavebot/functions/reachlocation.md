
# reachlocation

<!-- tabs:start -->

#### **English**

Walk to a coordinate.

#### **Portuguese**

Caminha até uma coordenada.


<!-- tabs:end -->

**reachlocation**(`x`, `y`, `z`, `rangeX*`, `rangeY*`)


- **Parameters**
  - `x:` coordinate x.
  - `y:` coordinate y.
  - `z:` coordinate z.
  - `rangeX:` optional param; range width, default is 1.
  - `rangeY:` optional param; range height, default is 1.


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Walk to the coordinates of [Venore Depot right stairs](https://tibiamaps.io/map#32935,32075,7:2), with the range of 1x1 (like a Stand).

```action
reachlocation(32935, 32075, 7, 1, 1)
```

2. Considering that in this example, this waypoint is an Action with coordinates at [x:32970, y:32085, z:6](https://tibiamaps.io/map#32970,32085,6:3) & range 3x1, if the character is not in front of NPC Digger(Venore magic shop), try to walk near him again.

```action
if (islocation() = false) then reachlocation(32970, 32085, 6, 3, 1)
```

