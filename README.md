git init
# → Reinitialized existing Git repository in .../.git/

git add .
# → added about_me.txt, projects/week2/hello_copy.txt (etc.)

git commit -m "Added project to git"
# → [master (root-commit) 6c29e2e] Added project to git
#   2 files changed, 3 insertions(+)
#   create mode 100644 about_me.txt
#   create mode 100644 week2/hello_copy.txt

git remote add origin https://github.com/Qudrot/my-first-project.git

# First push attempt failed (wrong branch name)
git push -u origin main
# → error: src refspec main does not match any

# Correct push (using master as default branch in my setup)
git push -u origin master
# → Enumerating objects: 5, done.
#   Counting objects: 100% (5/5), done.
#   ...
#   To https://github.com/Qudrot/my-first-project.git
#    * [new branch]      master -> master
#   Branch 'master' set up to track remote branch 'master' from 'origin'.
cd ~/documents
git clone https://github.com/Qudrot/my-first-project.git
cd my-first-project

touch goal.txt
nano goal.txt
# → typed some content, saved

git add goal.txt
git commit -m "Added my goals"
# → [master 7d8d1d0] Added my goals
#   1 file changed, 3 insertions(+)
#   create mode 100644 goal.txt

git push
# → Enumerating objects: 4, done.
#   ...
#   To https://github.com/Qudrot/my-first-project.git
#      6c29e2e..7d8d1d0  master -> master
