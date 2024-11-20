- 👋 Hi, I’m @Takpara
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...


<!---
Takpara/Takpara is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
The main reason I would use a template repository is so that all of the files I would typically use can be added to a template repository so that I don't have to add them each time you need to create a new repository. These files can be as simple as a customised .gitignore file, all the way up to a pre-defined template I use for an application.

Setup and use GitHub Repository Templates
Prior to starting, ensure you have the GitHub and git CLI tools installed and that you have authenticated your GitHub account with both of them.

Note: The template repository name used in the below example, my-template-repo, can be changed to whatever you would like it to be.

Create a Repository
First, open your CLI tool and create a normal GitHub repository, be that a public or private repository.

So, what does the above do? It will:

Create a repository called my-template-repo.
It will be a private repository (--private (change it to --public if you want it to be public)).
It will be cloned to the folder you are currently in (--clone).
A .gitignore file will be created with the defaults GitHub has for Python (--gitignore Python). Others are available for other languages.
The wiki section of the repository will be disabled (--disable-wiki).
An MIT license will be applied (--license MIT). Others are available or you can remove this if you don't want a license applied to the repository.

Change Folder
Navigate to the folder the repository was cloned to, which is typically the name of the repository: cd my-template-repo

Add Files to Folder
Place all of the files that you want into the folder and make any changes to the .gitignore file you want.

Add Files to a Commit
Add the files to be committed: git add .

Create a Commit
Create a commit for all the files that were added or changed: git commit -m "Base template files"

Push Commit to GitHub
Push the files to that repository: git push

Convert the Repository to a Template Repository
Convert the repository to a template repository: gh repo edit <your-github-username>/my-template-repo --template

If you look in the list of your repositories in your web browser, it will now show as Private Template, rather than just Private next to the repositories name.

Create a Repository Using the Template Repository
Now you can create a new repository from that template. Change my-new-repo to the name you want it to be and --public to --private if you need it to be a private repository:
gh repo create my-new-repo \
            --public \
            --clone \
            --template my-template-repo

Conclusion
In this article, we covered:

Creating a new repository that would be used as a template.
Converting that repository to be a template after the files have been added.
Finally, deploying a new repository from that template repository.


