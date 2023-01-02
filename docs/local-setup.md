### Local Setup
For playing around

I need:

-   Node Version 16 (It is recommended to use [volta](https://frontside.com/blog/2022-01-24-backstage-with-vscode/) or [nvm](https://github.com/nvm-sh/nvm) to manage node versions)
-   Yarn to manage dependencies
-   Git for source control

Run:
```
npx @backstage/create-app
```

![image](https://user-images.githubusercontent.com/13553866/210218620-75ffd24a-5722-4633-b27e-4cc3febe3813.png)



The script will copy Backstage’s template with directories and files and install all its dependencies.

![image](https://user-images.githubusercontent.com/13553866/210218697-eee32e4f-54df-4476-8b9b-f6a5932004d9.png)


When you navigate to the newly created directory, you’ll see the following structure:

```markdown
├── packages
│   ├── app
│   │   ├── package.json
│   ├── backend
│   │   ├── package.json
│   ├── index.js
├── app-config.yaml
├── catalog-info.yaml
├── package.json
├── lerna.json
└── .gitignore
```


To manage dependencies between the monorepo, Backstage uses [lerna](https://github.com/lerna/lerna), hence the lerna.json file.

Navigate to your instance’s directory in your terminal and run:
```
yarn dev
```
Now, let’s start making your Backstage instance more yours by changing its name. Go to your app-config.yaml file and change the app’s title to yours. In our case, it looks like this:

```
app:

	title: Terroir Portal

	baseUrl: [http://localhost:3000](http://localhost:3000)

organization:

	name: Terroir Technologies

```



