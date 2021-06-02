# CALCOFI Jupyter Book

## Quick start to running: 
- If necessary, pip install jupyter-book. If you're using conda, you may have to conda install jupyter-book (but I've never used conda so not 100% sure)
- Clone the repository, navigate to the directory, run "jupyter-book build ." (no quotes)
- You should see a _build/ directory. Either click the link in the terminal, or navigate to the _build/html directory and open index.html in a browser. You should now be able to see the website.

## Troubleshooting notes (add here as you see fit):
- I was getting a lot of issues with using the correct kernel. You may need to manually edit the metadata of the jupyter notebook you import to make sure the kernel is named correctly, following format in notebooks.ipynb
- To add a new page, you need to add it to _toc.yml (match what I did with correlations), and be sure the page has a title or it won't build. For jupyter notebook cells what I did was add a markdown cell at the very top that just had # Title
- If VSCODE isn't displaying an animated plot, try adding these lines of code above your plotting code:

    import plotly.io as pio
    
    pio.renderers.default = 'notebook'

- To control which code chunks are hidden completely or just hidden but viewable by clicking a button, go into Jupyter Notebook, click the "View" tab, and then the "tags" button. If you want to **completely omit a cell** (hide both input and output), add **"remove_input"** to the tag box. If you want to **hide a cell, but keep it's output**, add **"hide_input"** to the tag box. I couldn't find a way to do this in VSCode, so you have to open the .ipynb file in Jupyter with Anaconda.

## How to make changes to project
1) Make sure that your personal branch is updated with master branch (this can be done with the GitHub Desktop application)
    * change **'current repo'** to **'calcofi-book1'**
    * change **'current branch'** to your personal branch
    * in the menu, select **'branch' -> 'update from master'**
    * click on the **'push origin'** button that appears 
    
    Now your branch is up to date with the master branch, and you can make changes to it.
2) Clone personal branch to local computer
    * using the command line/terminal, navigate to desired folder
    * type **git clone -b "your branch_name" https://github.com/reznikovl/calcofi1-book.git** to copy your branch to your computer

3) Push changes to personal branch
    * in your working directory, type **git add .**
    * use **git commit -m "comment about changes"** to commit your changes
    * use **git push origin "your branch name"** to push changes to your personal branch
4) Create a pull request to the master branch

5) Optional: If you merged to master, and are confident that your build directory is correct and updated, and want to publish to the github pages website, you can run this command: ghp-import -n -p -f _build/html

Note: you need to run pip install ghp-import the first time you do so

  
