# Initial commit 
 
 1666  git init
 1667  dvc init
 1668  git commit -m "Init DVC"
 1669  git remote add origin https://pat@github.com/aneesarom/dvc_test.git
 1670  git config --global --add safe.directory /mnt/C006855D06855576/Anees/anees_personal_projects/dvc_test
 1674  dvc add dataset/
 1676  git add .
 1677  git commit -m "Add dataset to DVC"
 1682  git branch -m master main
 1683  git push -u origin main

# Dataset update

 1685  dvc add dataset
 1686  git add dataset.dvc
 1687  git commit -m "Update dataset after changes"
 1688  git push -u origin main

# Rollout

 1689  git log --oneline
 1690  git checkout d743f8a
 1691  dvc checkout
 1692  history