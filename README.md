# github-demo

A tiny shopping list for practising Git and GitHub: forking, cloning, pushing, and pulling.

## Practice exercise

### 1. Fork and clone

1. Click **Fork** at the top of this page to make your own copy.
2. Clone your fork (use the **HTTPS** URL instead if you don't have an SSH key set up):

   ```sh
   git clone git@github.com:<your-username>/github-demo.git
   cd github-demo
   ```

### 2. Push a change

3. Make a branch:

   ```sh
   git checkout -b add-<your-username>
   ```

4. Open `shopping-list.md` and add one item to the end of the list.
5. Commit and push to your fork:

   ```sh
   git add shopping-list.md
   git commit -m "Add <item> to shopping list"
   git push -u origin add-<your-username>
   ```

6. On GitHub, click **Compare & pull request** to send your change to the original repo.

### 3. Pull everyone else's changes

7. Connect to the original repo (only needed once):

   ```sh
   git remote add upstream git@github.com:churslic/github-demo.git
   ```

8. After the pull requests are merged, get the latest list:

   ```sh
   git checkout main
   git pull upstream main
   ```

9. Update your fork on GitHub:

   ```sh
   git push origin main
   ```
