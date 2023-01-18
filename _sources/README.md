# QuISP Textbook

![cover](cover.jpg "Cover")

## instruction to edit quisp-textbook
1. Create a new branch for your work, and checkout to that branch
2. write contents in a new file (e.g. `chapter1.md`). 
3. add an entry in `_toc.yml` (e.g. `- file: markdown-notebooks`)
4. Make a new PR to merge into the `main` branch.
5. (for publisher/administrator) after the working branch is merged, execute `jupyter-book build .` and then `ghp-import -n -p -f _build/html`. `ghp-import` will automatically push all the changes into the `gh-pages` branch. GitHub Actions will do the rest.
