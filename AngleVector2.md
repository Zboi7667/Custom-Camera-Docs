**Description:** A constructor to create an Angle, should only be used when setting Maximum/Minimum Angles on the [Camera](Camera.md) Object.

**Functions**
*new* ( maximum_right_angle , maximum_left_angle )

Code Example:
```lua
local Camera = require(THING)
Camera.MaxPitchAngle = AngleVector2.new(50,-50)
Camera.MinYawAngle = AngleVector2.new(5,-5)
```

Source:
```lua
Camera.AngleVector2 = {
    ["new"] = function(a,b)
        local Return = {}
        Return["AngleA"] = math.abs(a)
        Return["AngleB"] = math.abs(b)
        return Return
    end
}
```
