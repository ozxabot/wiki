{{ infobox_object({
	"id": 66,
	"name": "Game Manager",
	"category": "Game",
	"sublayer_width": 14
}) }}

Various I/O to control the level score and level completion.

The game ends if a value of 1 is sent to either **`IN0`** or **`IN1`**. If high scores are enabled, the game is lost, no high score is saved unless "Store high score on game over" is enabled.

The game may also end automatically if the final score specified in the level properties is reached.

**NOTE:** **`OUT0`** can be used to check whether the final score has been reached. You may want to use a [[Floor]] component to filter this value before you pass it on to binary devices, otherwise a value of 0.5 (half final score reached) will be rounded up to 1.

## Socket information
- **`IN0`**:  Player wins the game
- **`IN1`**:  Player loses the game
- **`IN2`**:  Score +1
- **`IN3`**:  Score +50
- **`IN4`**:  Score +100
- **`IN5`**:  Score +250
- **`IN6`**:  Score +500
- **`IN7`**:  Score -1
- **`IN8`**:  Score -50
- **`IN9`**:  Score -100
- **`IN10`**: Score -250
- **`IN11`**: Score -500
- **`IN12`**: Restart Level
- **`OUT0`**: Output current score as a fraction: `current_score/max_score`. If there is no max score, 0 is always output
