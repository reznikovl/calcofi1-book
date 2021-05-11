# CALCOFI Jupyter Book

## Quick start to running: 
[*] If necessary, pip install jupyter-book. If you're using conda, you may have to conda install jupyter-book (but I've never used conda so not 100% sure)
[*] Clone the repository, navigate to the directory, run "jupyter-book build ." (no quotes)
[*] You should see a _build/ directory. Either click the link in the terminal, or navigate to the _build/html directory and open index.html in a browser. You should now be able to see the website.

## Troubleshooting notes (add here as you see fit):
[*] I was getting a lot of issues with using the correct kernel. You may need to manually edit the metadata of the jupyter notebook you import to make sure the kernel is named correctly, following format in notebooks.ipynb
[*] To add a new page, you need to add it to _toc.yml (match what I did with correlations), and be sure the page has a title or it won't build. For jupyter notebook cells what I did was add a markdown cell at the very top that just had # Title