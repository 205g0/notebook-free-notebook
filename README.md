# notebook-free-notebook
## A professional, lock-in-free Jupyter dev env for coders, teams and non-trivial, large Jupyter projects

_Disclaimer: If you think there is nothing wrong with notebooks (.ipynb files) this post is not for you._

**Key features:**
- no .ipynb
- no vendor lock-in
- zero properietary tooling
- works with cloud or local TPUs out of the box
- super simple, no moving parts, just VS Code and a Jupyter kernel
- fast and easy setup
- optional vim binds
- free

![vscode.png](vscode.png)

Initially, I was impress by Jupyter and notebooks but found them quickly annoying (coming from a programming background). Getting the right IDE was not easy because there're many vendor-locked-in products, most .ipynb-based and lacking essential/typical dev features. I finally came to following solution which is rather for coders which is at the same time very simple but powerful and flexible:

- VS Code as front-end but **not** with VS Code's built-in notebook viewer[1]
- Instead I use **VS Code's Interactive Python Tab** which allows quick execution of one cell with `Ctrl-Enter` or all above cells
- The Interactive Tab shows the cell outputs in **chronological order**
- The **execute above cells** feature is quite handy, it's located at every cell and let you run the entire notebook till that button
- **vim binds** via the vim plugin[2]; fwiw, this setup is the only with proper vim binds next to Google's Colab
- The Jupyter kernel runs on a beefy remote machine (any kind of bare-metal TPU-based machine in the cloud, under you desk, etc.) connected to VS Code; the Jupyter Notebook or Lab interface is not used
- **Images are rendered;** sounds like a minor thing but it's not, before I sent via vim-slime commands to a tmux tab with IPython which is a similar setup but I couldn't render images because it's in the terminal
- Easy shareable and git-committable `.py` files which have all the notebook data in the convinient *percent format*
- Any further shortcuts above the vim layer can be defined
- Free as in free lunch

I found this setup painless, scalable and most important fluid. No manual back and forth between cells but one file of code with easy, instant navigation via vim binds. No cloud notebook vendor lock-in and a super simple setup.

It is for teams (fully git-able and human-readable in contrast to .ipynb), scalable and in particular for non-trivial, larger projects because it clearly separates (one of the most flexible) frontends and TPUs without locking in the users into anything.

Give a user 8x A100 and he does the entire dev setup in 5 minutes incl. OS installation of the TPU machines and it doesn't matter if the TPUs are in the cloud or under his desk haha, no lock-in nowhere. Or give this setup to a friend and he will git clone my model 1:1 and run it within seconds on his new 3090. Or another peer who prefers vim binds because it might be easier to explore/do his own experiments/navigate through huge code bases for hours. Or a data scientist who prefers the .ipynb format, one click and voilà, he can work in the notebook format. IDK of any other free IDE that allows such flexibility without any lock-in.

[1] VS Code's built-in native `.ipynb` viewer is good but it does not support any vim bind extension and I still think the notebook paradigm is not the right one. For learning and following tutorials in the beginning it's great but once you interact more than you read it slows you down.

[2] vim binds have a steep learning curve but once you have the muscle memory you should be faster when dealing with large code bases (different discussion but just to clarify my requirements in this regard)
