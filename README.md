fmECG Project is a biomedical system for measuring electrogram data using Flutter for Mobile App, NextJS for back-end and ReactJS for web admin.

> [!IMPORTANT]
> In this project, team decides to separate web and server into 2 independent component with new repo. This repo will be marked as archived and not maintained. Reference only.


## 📒 Installation
- [Normal Installation](https://github.com/techcomrade/fmECG/wiki/%5BInstallation%5D-Manual)
- [Installation with Docker](https://github.com/techcomrade/fmECG/wiki/%5BInstallation%5D-With-Docker)

## 📦 Features
- Measure heart rate, blood pressure real-time with BLE connection between hardware device and mobile app
- Manage doctors, patients data from web system
- Connect doctors and patients through Chat Services with Web Socket

## 🔆 Read more

- [Commit code using Git Tortoise](https://github.com/techcomrade/fmECG/wiki/%5BTools%5D-S%E1%BB%AD-d%E1%BB%A5ng-Git-Totories-khi-commit-code)
- [Auto deployment flow with Github Actions and Docker](https://github.com/techcomrade/fmECG/wiki/%5BWorkflow%5D-Auto-deploy-system-with-Docker-and-Github-Actions)
- [Database migrations with Sequelize](https://github.com/techcomrade/fmECG/wiki/%5BWorkflow%5D-Database-Migrations)

## 📒 Luồng viết code
- Tạo model trong folder entities map 1:1 với thực thể trong database
- Trong modules tạo các folder tương ứng với các thực thể
    + repository : thực hiện các câu query
    + service : xử lý logic
    + module : import và export các lớp (service, repository, controller). Chú ý export module và import module cần thiết 
    + controller : nhận các request từ frontend 

## 📒 Run migration and seed data
- checkout sang nhánh 'development' hoặc 'ECG_20241' 
- git pull để kéo code mới nhất về
- npm install : cài đặt các thư viện cần thiết
- Chỉnh sửa password tương ứng với mysql workbench trên máy
- npm run db:reset
- npm run db:migrate
- npm run db:seed

## Run code with git-crypt
Project is using git-crypt to encrypt all credentials, contributors need to contact to repo's owner to get decryption key.

Install `git-crypt`: [MacOS, Ubuntu](https://github.com/AGWA/git-crypt/blob/master/INSTALL.md), [Windows](https://github.com/oholovko/git-crypt-windows?tab=readme-ov-file#git-crypt-for-windows)

After saving key somewhere in your directory, command:
```bash
git-crypt unlock <path_to_key>
```
If all files are decrypted, done! You can run code normally.

