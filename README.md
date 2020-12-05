# notebook-free-notebook
## A Jupyter dev env for coders

When I started with Python's data stack I was impressed by Jupyter and notebooks but found notebooks quickly annoying (coming from a programming background). I finally came to a great solution rather for coders than for data scientists:

- VS Code as front-end but **not** with VS Code's built-in notebook viewer[1]
- Instead I use **VS Code's Interactive Python Tab** which allows quick execution of one cell with `Ctrl-Enter` or all above cells
- The Interactive Tab shows the cell outputs in **chronological order**
- The **execute above cells** feature is quite handy, it's located at every cell and let you run the entire notebook till that button
- **vim binds** via the vim plugin, not the nvim plugin yet, latter has still some issues with scrolling
- The Jupyter kernel runs on a beefy remote machine connected to VS Code
- **Images are rendered;** sounds like a minor thing but it's not, before I sent via vim-slime commands to a tmux tab with IPython which is a similar setup but I couldn't render images because it's in the terminal
- Easy shareable and git-committable `.py` files which have all the notebook data in the convinient *percent format*
- Any further shortcuts above the vim layer can be defined
- Free as in free lunch

I found this setup painless, scalable and most important fluid. No manual back and forth between cells but one file of code with easy, instant navigation via vim binds. No cloud notebook vendor lock-in and a super simple setup.

[1] VS Code's built-in native `.ipynb` viewer is very good but it does not support any vim bind extension and I still think the notebook paradigm is not the right one. For learning and following tutorials in the beginning it's great but once you interact more than you read it slows you down.
