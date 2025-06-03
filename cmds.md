## Local storage

# Initial commit 
 
*  git init
*  dvc init
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

## Remote Storage

1710  git init
1711  dvc init
1714  dvc remote add dataset gdrive://<folder_id>
1717  dvc add dataset/
1718  git add .gitignore dataset.dvc
1719  git config --global --add safe.directory folder_path

https://dvc.org/doc/user-guide/data-management/remote-storage/google-drive#using-service-accounts

1727  dvc remote modify dataset gdrive_use_service_account true
1728  dvc remote modify dataset --local gdrive_service_account_json_file_path /path/of/dvc_secrets.json

# Make it google drive folder access to anyone with the  link

1729  dvc push
