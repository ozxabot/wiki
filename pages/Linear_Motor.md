{{ infobox_object({
	"id": 22,
	"name": "Linear Motor",
	"category": "Robotics",
	"sublayer_width": 15
}) }}

A linear motor attempts to move its pivot to the target end of the motor. Power the motor by connecting it to a controller (CT) using an [[Interface Cable]] (blue cable).

**Properties:** Speed/force trade-off, size

Speed/force (internal gearing) allows you to control the trade-off between the speed of the motor and the force of the motor.

Errors are reported through the interface if the motor is unable to move, unless it has reached its final position (any of the two ends depending on direction). Errors are always reported if the motor is moving in the wrong direction.

## Socket information
- **`IN0`**: Interface socket
