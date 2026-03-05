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

### Quick Links
- Installing the prerequisites
- Run the static generated website locally
- Create a static generated website
- How to host your website
- Creating a resume

> Note: These instructions are specifically created for Linux users. The steps to perform these instructions may be different if you are using Windows.

Following Andrew Etter's guide on Technical Documentation, the instructions are formatted in a way such that the target audience can understand. Headings and ordered lists are also used to make it easier to scan and read.
### 1 Setup 
Before proceeding to further steps, you will have to install 3 prerequisites: Python, Pelican (the static website generator we will use)
1. Open the command line terminal
2. [Python](https://www.python.org/downloads/) is already pre-installed in Linux. Verify that the version is 3.10 or above by typing:
```bash
python --version
```
*If the version is < 3.10, update it by typing*
```bash
sudo dnf update
```
3. Install Pelican with:
```bash
python -m pip install "pelican[markdown]"
```
5. Verify that everything is installed by typing each of the following:
```bash
pelican --version
python --version
```
The output should show the version for each of these packages.
### 2 Running the Pelican website locally
In this step, you will learn how run the static generated website. Git is required in order to complete these steps which is already installed by default on Linux.   
#### 2.1 Clone this repository
1. In this repository, copy the Codeberg URL beside the HTTPS icon located at the top right. 
2. Verify that URL you copied is this: `https://codeberg.org/samsoncj/comp2600-a2.git`
3. In the command line terminal, clone this repository by typing `git clone [URL]`. The command should look like this: 
```bash
git clone https://codeberg.org/samsoncj/comp2600-a2.git
```

> Note: You only have to do this once. The same step applies for any other repositories. The only difference is the URL. Ensure that you are copying the correct URL for the repository you want to clone.
#### 2.2 Run the website locally
1. Navigate to the project directory you cloned using `cd`. 
2. Type `pelican content` to regenerate the static site.
3. Type `pelican --listen` to start the website locally.
4. The URL for the website will show. Hold CTRL and click this URL to launch this website in the web browser.
5. The main page of my website should load.
### 3 Create your own Pelican website
In this step, you will be using a distributed version control system (DVCS) to host the source code of the static website that you will be creating. Etter recommends that we should store our documentation in the same repository as the source code. We will be using Git as our DVCS and Codeberg to store our source code.

1. First, create a new repository in Codeberg by clicking the `+` icon on the top right of the page.
2. Enter a repository name in the Repository name field then click Create.
3. Clone this repository. 
	- If you are unsure on how to do this, refer to the section **2 Running the Pelican website locally**
4. Once the repository is cloned, make sure to navigate to that cloned repository
5. Create a Pelican skeleton project
```bash
pelican-quickstart 
```
7. You will be prompted to enter the details of your website. 
	- The URL prefix should be: `https://username.codeberg.page/repositoryname`
	- Example: `https://samsoncj.codeberg.page/comp2600-a2`
8. Publish the website 
```bash
pelican content
```
7. You have just created a skeleton of your website! Enter `pelican --listen` in the command line to see your website locally.

