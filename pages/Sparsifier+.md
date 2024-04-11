{{ infobox_object({
	"id": 51,
	"name": "Sparsifier+",
	"category": "Signal-i1o1",
	"sublayer_width": 14
}) }}

Output 1 if **`IN0`** is not equal to the last value of **`IN0`**. Essentially, bit noise is smoothed out and coherent signal streams are turned into sparse noise whenever it changes.

**Example 1:** `00001111000010` -> `00001000100011`

**Example 2:** `01010101` -> `01111111`

Use this gate to do, for example, nothing. :(

## Socket information
- **`IN0`**: Input signal
- **`OUT0`**: Sparsified output signal
