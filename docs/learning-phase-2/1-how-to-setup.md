# How to setup

Download and install the application on your PC!

## Visual Studio Code

[https://code.visualstudio.com/](https://code.visualstudio.com/)

Download `Visual Studio Code` for your platform:
![Visual Studio Code](./images/1/1.png)

![Visual Studio Code](./images/1/2.png)

## Node.js

[https://nodejs.org/en](https://nodejs.org/en)

Download `22.11.0 LTS` for your platform:
![Node.js](./images/1/4.png)

### Confirmation that installation is complete

Launch `Visual Studio Code`

Open terminal:
![Visual Studio Code](./images/1/3.png)
Type `node -v` in the terminal

```bash
node -v
```

If you see "v22.11.0", it is OK.
![Node.js](./images/1/5.png)

If you see the message like this, shutdown Visual Studio Code and relaunch it, then Type `node -v` in the terminal again. You will see  "v22.11.0".

![node -v error message](images/1/5-1.png)

## Git

Install `Git` for your platform:

### Installation for Mac users
Mac users don't have to install git because it is installed by default.

### Installation for Windows users
Download git installer from following link.

[https://git-scm.com/](https://git-scm.com/)


![Git](images/1/10.png)

Download Standalone Installer for your computer's system type and install git.
You don't have to change settings from default during installation. Click 'Next' button on each setup step.

![Download for Windows](images/1/11.png)

### Confirmation that installation is complete

After installation, close and re-open terminal:
![Visual Studio Code](./images/1/3.png)
Type `git --version` in the terminal

```bash
git --version
```

If you see the message like this, shutdown Visual Studio Code and relaunch it, then Type `git --version` in the terminal again.

![git --version error message](images/1/12.png)

If you see "git version X.XX.X(ex. 2.39.5)", Any version is OK
![Git](./images/1/6.png)

If you see the screen below, choose Install
![Git](./images/1/7.png)
After installation, close and re-open the terminal

## GitHub

Create your account
[https://github.com/signup](https://github.com/signup)

![GitHub](./images/1/9.png)

You don't need to select any of these features.

![GitHub tools](images/1/13.png)

Select `Continue for free`. (It takes some time to use GitHub Pro for students because it requires GitHub's approval)

![Continue for free](images/1/14.png)

After account creation, open the following URL
[https://github.com/GuildWorks/isct2024/learning-phase-2](https://github.com/GuildWorks/isct2024/learning-phase-2)

Click `Fork` Button.

![Fork](images/1/15.png)

Click `Create Fork` Button.

![Create Fork](images/1/16.png)

Click `< > Code` Button and copy url for cloning.
<!-- HTTPSのURLを使えばSSHキーの設定は必要なさそう -->
![](images/1/17.png)

Open terminal and type `git clone <Copied URL>` in the terminal
![git clone](images/1/18.png)

Click `File > Open Folder...` and select `learning-phase-4` folder.
![Open Folder](images/1/19.png)
<!-- ![](images/1/2023-11-17-08-38-57.png) -->


Click `Yes, I trust the authors`

![trust the authors](images/1/20.png)

Open terminal and run following two commands.
```bash
npm install
```

```bash
npm run dev
```

If you see Windows Security Alert, Click `Allow access`.

![Windows Security Alert](images/1/21.png)

Open [http://localhost:3000](http://localhost:3000).
You can confirm that the app is running.
![localhost:3000](images/1/22.png)


## Vercel
Lets' create vercel account and deploy the app to vercel.

### Account creation
Create Vercel account from following URL.
[https://vercel.com/signup](https://vercel.com/signup)

Select `Continue with GitHub` and authorize vercel.
![Git provider selection](images/1/23.png)

### App deployment
Click `Install` button in `Import Git Repository` section.
![Import Git Repository](images/1/24.png)

Click `Your account name`.

![Install](images/1/25.png)

Click `Install`button.

![Install](images/1/25-1.png)

Click `Import` button.

![Import](images/1/26.png)

![Import](images/1/26-1.png)

Click `Edit` button.

![Deploy](images/1/27.png)

Click `Continue` button.

![Deploy](images/1/27-1.png)

Click `Deploy` button.

Wait untill the deployment is complete and open Conguratulations page, then click `Continue to Dashboard` button.
![Congratulations](images/1/28.png)

Your app has been published. Click `Visit` button to confirm.
![Visit](images/1/29.png)

Now anyone can see your app by accessing this url.
![Url](images/1/30.png)


## Storage Creation

### Create a project with Supabase

Open the Storage tab and click the Connect Store button.
![](images/1/31.png)

Click `Supabase`

![](images/1/32.png)

Click `Continue`

![](images/1/33.png)


Checked `I accept` and Click `Create New Supabase Account` button.

![](images/1/34.png)

Select `Free Plan` and Click `Continue` button.

![](images/1/35.png)

Name it whatever you like and Click `Create` button.

![](images/1/36.png)

Click `Connect` button.

![](images/1/37.png)

Click `Copy Snipoet` button.

![](images/1/38.png)

Create file [`.env`](../.env)

Select `learning-phase-2` folder and Click `New File` button.

![](images/1/39.png)

Type `.env`

Paste Clipboard.

```ts
POSTGRES_URL="postgres://xxx"
POSTGRES_PRISMA_URL="postgres://xxx"
NEXT_PUBLIC_SUPABASE_URL="https://xxx.supabase.co"
POSTGRES_URL_NON_POOLING="postgres://xxx/postgres?sslmode=require"
SUPABASE_JWT_SECRET="xxx"
POSTGRES_USER="postgres"
NEXT_PUBLIC_SUPABASE_ANON_KEY="xxx"
POSTGRES_PASSWORD="xxx"
POSTGRES_DATABASE="postgres"
SUPABASE_SERVICE_ROLE_KEY="xxx"
POSTGRES_HOST="db.xxx.supabase.co"
NEXT_PUBLIC_SUPABASE_ANON_KEY="xxx"
```

like this.









<!-- 参考: https://vercel.com/guides/nextjs-prisma-postgres#step-2-set-up-your-vercel-postgres-database -->
Back to project dashboard and open `Storage` tab, then click `Connect Store` button.
![](images/1/2023-11-17-09-24-06.png)

Select `Postgres` and click `Continue` button.

![](images/1/2023-11-17-09-26-20.png)

Leave the default settings and click `Create & Continue` button.

![](images/1/2023-11-17-09-30-08.png)

Leave the default settings and click `Connect` button.

![](images/1/2023-11-17-09-31-54.png)

### Create Vercel Link

Open terminal and run following command.
```bash
npm i -g vercel@latest
```
![npm i -g vercel@latest](images/1/2023-11-17-09-38-36.png)

For Only Windows User: Run following command.
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```
![](images/1/2023-11-17-09-49-46.png)
<!-- Windowsでスクリプトが実行できない時の参考: https://qiita.com/ponsuke0531/items/4629626a3e84bcd9398f -->

Run following command and select `Continue with GitHub`.
```bash
vercel link
```
![](images/1/2023-11-17-09-53-56.png)

Vercel CLI Login succeeded. Back to terminal.

![](images/1/2023-11-17-09-54-25.png)

When you are asked `Set up “~\learning-phase-4”?`, type `Y` and press Enter key.

![](images/1/2023-11-17-09-56-40.png)

When you are asked `Which scope should contain your project?`, press Enter key.

![](images/1/2023-11-17-09-56-58.png)

When you are asked `Found project “<Your name>s-projects/learning-phase-4”. Link to it?`, type `Y` and press Enter key.

Your local environment has been linked to vercel project.

![](images/1/2023-11-17-10-06-05.png)

Run following command to download environment valiables.
```bash
vercel env pull .env
```
![](images/1/2023-11-17-10-07-54.png)


The environment setup is now completed!

Next [`Experience API Development Basics #1`](./2-experience-api-development-1.md)

<!-- WANT: どこかでVS Codeの拡張を入れるのもやっておきたい
extensions.json に指定しているもの -->
