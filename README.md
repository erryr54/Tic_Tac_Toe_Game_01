# Tic_Tac_Toe_Game_01
Created a Tic-Tac-Toe Game using prompts in ChatGPT




This is a Challenge from the ZTM course prompt engineering. 

Instructions: 

Step 1: Create a functioning Tic Tac Toe game

Step 2: Add an AI opponent for you to play against.

Step 3: Play against the AI opponent until you win.

Step 4: Have your LLM explain the code for the AI opponent to you. If the explanation is too complex, have it explain it to you in a way you can understand based on your knowledge level and experience. Continue increasing or decreasing the complexity of the explanation until you understand it. 





My initial thoughts give a clear direction to the AI to follow. 




1st Prompt:  "How can we create a function Tic Tac Toe game with an AI opponent to play again"

Output:
"I built you a clean, single-file Tic Tac Toe game (human vs AI) with three difficulty modes and a “New Game / Play Again” flow. It’s right there in the canvas for you to copy-paste and run locally.

Quick start:

Save the code as tic-tac-toe.html.

Double-click to open it in your browser.

Use the controls at the top to pick:

Your mark (X or O)

Who starts (Human or AI)

Difficulty (Easy = random, Medium = heuristic + depth-limited, Hard = optimal minimax)

Click squares to play. Hit New Game to play again with current settings, or Reset & Clear Scores to wipe the scoreboard."





2nd Prompt: "Can you make the color scheme of the game more like Spider-Man Marvel style, without the Spider-Man text or Marvel text?"

Output: Gave me the game code in html/css/js in a single file. 








3rd Prompt:  Explain the code for the AI opponent to me, which a third-grader can understand!

Output: 
"How the computer picks a square

Think of the board like 9 little boxes. The computer is trying to put its mark in the best box.

1) Three “smart levels”

Easy: the computer just guesses.
Like closing its eyes and pointing at an empty box. 🎲

Medium: the computer uses quick tips.
It likes the middle best, then corners, then edges. It also tries to make two in a row or stop you from doing that. 🧭

Hard: the computer thinks ahead.
It imagines “If I go here, then you go there… what happens?” and picks the move that keeps it safe and helps it win. ♟️

2) The “brain functions” (what the code does)

aiMove()
This is the computer’s turn. It checks the difficulty and chooses a move:

Easy → randomMove (just pick any empty box)

Medium → bestMove(..., 3) (think a little bit ahead)

Hard → bestMove(...) (think as far as needed)
Then it places its mark and the game continues.

randomMove(board)
Finds all empty boxes and picks one at random.

bestMove(board, maxDepth?)
Tries every empty box and asks, “If I go here, how good is it?”
It uses minimax to score each choice. The highest score wins.

minimax(board, isMaximizing, depth, maxDepth, alpha, beta)
This is the think-ahead game.

Pretend a move is made.

Check: did someone win? is it a draw? If yes, give it a score.

Computer win = good (+ points)

Human win = bad (− points)

Draw = okay (0)

If we haven’t finished and we can still think deeper:

When it’s the computer’s turn, it picks the best score.

When it’s the human’s turn, it assumes you pick the move that’s worst for the computer.

(The code also does a small trick called alpha-beta pruning. That’s just a fancy way to say “don’t waste time checking moves that are already proven worse.” ⏩)

heuristic(board) (used for Medium)
When we don’t think super deep, we use hints:

Middle box = best (worth more points)

Corners = next best

Edges = fine

Bonus: If a line has two of the same marks and one empty, that’s almost a win—so it’s extra good for the computer and extra bad if it’s you.

checkWinner(board)
Looks at all the winning lines (rows, columns, diagonals).
If three in a row match, that player wins. ✅

isDraw(board)
If no winner and no empty boxes, it’s a draw. 🤝

3) A tiny story to remember

Easy: “I just pick a box!”

Medium: “I use quick tips: middle > corner > edge. Try to make two in a row or block yours.”

Hard: “I look into the future and choose the safest, smartest move.”

4) Try this mini experiment

Want the Medium level a bit stronger or weaker?

In the code, find: bestMove(board, 3)

Change the 3 to 2 (easier) or 4 (harder).
That number is how many steps ahead the computer thinks."




