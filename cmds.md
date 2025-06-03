# Local storage

## Initial commit 
 
*  git init
*  dvc init
*  git commit -m "Init DVC"
*  git remote add origin https://pat@github.com/aneesarom/dvc_test.git
*  git config --global --add safe.directory /mnt/C006855D06855576/Anees/anees_personal_projects/dvc_test
*  dvc add dataset/
*  git add .
*  git commit -m "Add dataset to DVC"
*  git branch -m master main
*  git push -u origin main

## Dataset update

 *  dvc add dataset
 *  git add dataset.dvc
 *  git commit -m "Update dataset after changes"
 *  git push -u origin main

## Rollout

 *  git log --oneline
 *  git checkout d743f8a
 *  dvc checkout
 *  history

# Remote Storage

*  git init
*  dvc init
*  dvc remote add dataset gdrive://<folder_id>
*  dvc add dataset/
*  git add .gitignore dataset.dvc
*  git config --global --add safe.directory folder_path

https://dvc.org/doc/user-guide/data-management/remote-storage/google-drive#using-service-accounts

*  dvc remote modify dataset gdrive_use_service_account true
*  dvc remote modify dataset --local gdrive_service_account_json_file_path /path/of/dvc_secrets.json

## Make it google drive folder access to anyone with the  link

*  dvc push
