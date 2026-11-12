# modern-code-review
lecture 10

This repository demonstrates the Modern Code Review (MCR) workflow using GitHub Pull Requests. An initial version of the 3×3 Tic-Tac-Toe game (game.py) was submitted via a feature branch, reviewed line-by-line by team members (and GitHub Copilot), and iteratively improved before merging into main.

👥 Team Members & Roles

Author (A)
Xu Yuming
11750870
Repository setup, initial implementation, PR creation, and defect resolution

Reviewer 1 (R1)
Xie Ting
11750765
Code style, unused variables, and refactoring repetitive logic (DRY principle)

Reviewer 2 (R2)
Li Yitong
11750844
Core game logic (0-based indexing, cell occupancy checks, and 9th-move tie handling)

Reviewer 3 (R3)
Xie Jingyi
11729869
Input validation (try-except, range checks) and requirement consistency ('X' / 'O')

Reviewer 4 (R4)
Li Ying
11729510
Turn-switching readability and modular board display (print_board)

🚀 How to Run
1. Make sure you have Python 3 installed.

2. Clone this repository or download game.py:
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

3. Run the game in your terminal:
python game.py

4. Players take turns entering row and column coordinates separated by a space (e.g., 1 2 for row 1, column 2, where values are between 1 and 3).
🛠️ Key Improvements Made During Code Review
• Fixed Index Out-of-Bounds Bug: Converted 1-based user coordinates [1..3] to 0-based list indices [i - 1][j - 1].
• Prevented Cell Overwriting: Added validation to ensure players cannot place a mark on an already occupied cell.
• Fixed 9th-Move Win/Tie Conflict: Replaced if n == 8: with a for ... else: construct so "Tie!" is only displayed when no player wins on the final move.
• Matched Game Specification: Replaced digit '0' with capital letter 'O' for Player 2.
• Added Robust Input Validation: Handled non-integer inputs and out-of-range coordinates gracefully without crashing.
• Refactored Code Structure: Simplified is_win() using loops, streamlined turn switching with n % 2 == 0, and extracted board rendering into print_board().
