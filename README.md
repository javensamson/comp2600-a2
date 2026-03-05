# Pelican Generated Website
Welcome to my repository! This repository contains the source code of my static generated website. The website is hosted by Codeberg Pages.

This document will help users who are interested in creating and hosting their own static generated website. The users that will perform these instructions are expected to know how to use Markdown and the command line terminal. 

## Prerequisites
This document assumes you have the following:
- Markdown editor
- Command line terminal
- Internet connection
- Python version 3.10 or above
- Codeberg account
- Git
## Instructions
>[!NOTE]
> These instructions are specifically created for Linux users. The steps to perform these instructions may be different if you are using Windows.

### Quick Links
- Installing the prerequisites
- Run the static generated website locally
- Create a static generated website
- How to host your website
- Creating a resume


Following Andrew Etter's guide on Technical Documentation, the instructions are formatted in a way such that the target audience can understand. Headings and ordered lists are also used to make it easier to scan and read.
### 1 Setup 
Before proceeding to further steps, you will have to install 3 prerequisites: Python, Pelican (the static website generator we will use).
1. **Open** the command line terminal
2. **Verify** that the version is 3.10 or above by typing:
```bash
python --version
```
* If the version is < 3.10, update it.
```bash
sudo dnf update
```
3. **Install** Pelican with:
```bash
python -m pip install "pelican[markdown]"
```
5. **Verify** that everything is installed by typing each of the following:
```bash
pelican --version
python --version
```
> The output should show the version for each of these packages.
### 2 Running the Pelican website locally
In this section, you will learn how run the static generated website. **Git** is required in order to complete these steps which is already installed by default on Linux.   
#### 2.1 Clone this repository
1. **Copy** the Codeberg URL in this repository. 
2. **Verify** that URL you copied is this: `https://codeberg.org/samsoncj/comp2600-a2.git`
3. **Clone** this repository with `git clone`. 
```bash
git clone URL
# Where URL is the repository URL you copied
# In this case it is https://codeberg.org/samsoncj/comp2600-a2.git

# It should look like this
git clone https://codeberg.org/samsoncj/comp2600-a2.git
```
> [!NOTE]
> You only have to do this once. The same step applies for any other repositories. The only difference is the URL. Ensure that you are copying the correct URL for the repository you want to clone.
#### 2.2 Run the website locally
1. **Navigate** to the project directory you cloned using `cd`. 
```bash 
 cd /comp2600-a2 # if you cloned a different repository replace comp2600-a2 with that repository name
```
2. **Regenerate** the static site
```bash
pelican content
```
3. **Start** the website locally.
```bash
pelican --listen
```
4. **Copy-paste** the URL to a web browser.
5. The main page of my website should load.
### 3 Create your own Pelican website
In this section, you will be using a distributed version control system (DVCS) to host the source code of the static website that you will be creating. Etter recommends that we should store our documentation in the same repository as the source code. We will be using Git as our DVCS and Codeberg to store our source code.

1. First, **create** a new repository in Codeberg by clicking the `+` icon on the top right of the page.
2. Enter a repository name in the Repository name field.
3. Click **Create**.
4. Clone this repository. 
	- Unsure on how to do this? Refer to [2.1 Clone this Repository](#21-clone-this-repository)
5. **Navigate** to that cloned repository.
```bash
cd /your-repository-name
```
5. **Create** a Pelican skeleton project.
```bash
pelican-quickstart 
```
6. You will be prompted to enter the details of your website. 
	- The URL prefix should be: `https://username.codeberg.page/repositoryname`
	- Example: `https://samsoncj.codeberg.page/comp2600-a2`
7. **Publish** the website 
```bash
pelican content
```
8. **You have just created a skeleton of your website!** 
9. Enter `pelican --listen` in the command line to see your website locally.
