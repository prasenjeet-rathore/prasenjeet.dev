+++
date = '2026-01-06T18:45:35+01:00'
draft = true
title = 'Free blog using Hugo and Github Pages'
+++

I wanted to create my own website for blogging without paying any monthly subscription for any services. Also want it to be minimal where I can just focus on writing using Markdown once the setup is done. Also i wanted the website to have fast loading time. All these things are very well taken care by Hugo and Github Pages. If you also would like to have a similar blog setup then this tutorial will be helpful hopefully.

### Step 1: Install Hugo
Begin by installing Hugo on your system. If you're using Fedora, you can easily install it using the terminal:
```bash
sudo dnf install hugo
```
For other operating systems, refer to the official installation guide on the [Hugo website](https://gohugo.io/installation/).

### Step 2: Create a New Hugo Site
Once Hugo is installed, create a new Hugo site using the following command:
```bash
hugo new site blog -f yml
```
This will generate a basic Hugo site structure with default directories.

### Step 3: Choose a Theme
Next, download a theme for your blog. In this tutorial, we'll use the "paper" theme but you can use any other themes, personally I like hextra, but paper theme is more easy to setup for this tutorial:
```bash
git submodule add https://github.com/nanxiaobei/hugo-paper themes/paper
```
After adding the theme, update the configuration file (`config.yml`) to set the theme to "paper".

### Step 4: Create a Demo Post
Create a demo post to test your setup:
```bash
hugo new posts/test.md
```

### Step 5: Set Up GitHub Repository
Create a new repository on GitHub with the name "blog". Then, initialize the local repository and push the files to GitHub:
```bash
echo "# blog" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/<your-github-username>/blog.git
git push -u origin main
```

### Step 6: Configure GitHub Pages
Navigate to the settings of your GitHub repository and access the "Pages" tab. Choose GitHub Actions as the build and deployment method, and select Hugo as the workflow. Click the green "Commit changes" button after the YAML file is generated.

### Step 7: Sync Local and Remote Repositories
Before making any further changes locally, synchronize your local repository with the remote one by running `git pull`.

### Step 8: Update Configuration
Update the `baseURL` in the `config.yml` file to reflect your GitHub Pages URL. Here's an example of the `config.yml` file contents:
```yaml
baseURL: "<enter your link from GitHub Pages section in the settings>"
languageCode: en-us
title: Blog
theme: paper
```