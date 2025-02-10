# project-1-game
"Snake, Water, Gun is a fun, simple hand game for two players, similar to Rock, Paper, Scissors. Each player simultaneously chooses one of three options: snake, water, or gun. 
# Snake, Water, Gun Game

This is a simple Python implementation of the classic game "Snake, Water, Gun." The game is played between the computer and a person. The rules are as follows:

- **Snake (s)** beats **Water (w)**
- **Water (w)** beats **Gun (g)**
- **Gun (g)** beats **Snake (s)**

If both the computer and the person choose the same option, the game is a tie.

## How to Play

1. **Run the Python script** in your preferred Python environment.
2. **Input your choice** when prompted:
   - `s` for Snake
   - `w` for Water
   - `g` for Gun
3. The **computer will randomly select** one of the three options.
4. The **result** will be displayed, indicating whether you won, lost, or if the game was a tie.

## Code Explanation

### Function: `gamewin(computer, person)`

This function determines the winner based on the choices of the computer and the person.

- **Parameters:**
  - `computer`: The choice made by the computer (`s`, `w`, or `g`).
  - `person`: The choice made by the person (`s`, `w`, or `g`).

- **Returns:**
  - `True` if the person wins.
  - `False` if the computer wins.
  - `None` if the game is a tie.

### Main Game Logic

1. The **computer's choice** is determined using `random.randint(1, 3)`:
   - `1` corresponds to Snake (`s`).
   - `2` corresponds to Water (`w`).
   - `3` corresponds to Gun (`g`).

2. The **person's choice** is taken as input from the user.

3. The `gamewin` function is called with the computer's and person's choices.

4. The **result** is printed based on the return value of the `gamewin` function:
   - If `None`, the game is a tie.
   - If `True`, the person wins.
   - If `False`, the computer wins.

## Example Output

```
computer turn: snake(s), water(w), gun(g)
person turn: snake(s), water(w), gun(g)
computer chose s
person chose w
you lose
```

## Requirements

- Python 3.x
- `random` module (included in Python's standard library)

## How to Run

1. Save the code in a file, e.g., `snake_water_gun.py`.
2. Run the script using Python:
   ```bash
   python snake_water_gun.py
   ```

Enjoy the game!
