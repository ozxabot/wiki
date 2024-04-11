{{ infobox_object({
	"id": 179,
	"name": "Sequencer",
	"category": "Signal-misc",
	"sublayer_width": 14
}) }}

Traverses over its given sequence at the given speed, outputting the value to **`OUT0`**.

The number of steps is calculated by the number of zeroes and ones in the "Sequence" field of its config dialog. The step width values work similar to the timer, meaning when the time specified has been reached, the sequencer will step one step forward in its sequence. The Wrap around option specifies whether or not the sequence should repeat once it has reached its end.

## Socket information
- **`IN0`**: Activate (on by default)
- **`OUT0`**: The current signal to output, whether its current step in the sequence is a 1 or a 0
