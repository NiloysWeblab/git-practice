<!--Markdown Practice-->
# Git and GitHub Note

Here is my **Git** and **GitHub** practice note, where I have documented important commands, concepts, and workflows related to version control and repository management.  

It will help anyone who follows this note to learn Git and GitHub just as I have.

## What is Git?

**Git** is a tool that helps manage and track changes in code.  

- It saves different versions of a project so you can go back if needed.  
- Multiple people can work on the same project without overwriting each other’s work.  
- You can create separate branches to try new ideas safely.  
- It allows merging, so changes from different people can be combined easily.  
- Git works on your computer but can also sync with online platforms like GitHub.
## Are Git and GitHub the same?

Git and GitHub are not the same, but they work together.

- Git is a tool that helps you track and manage changes to your code on your computer. It keeps a history of every change you make, so you can go back to previous versions if needed.

- GitHub is a website where you can store your Git repositories (code projects) online. It also helps you share your code with others and collaborate easily.

## Why Learning Git and GitHub is Important

Learning Git and GitHub is an essential skill for anyone interested in software development. Here’s why:

- **Collaboration Made Easy:** Git lets multiple developers work on the same project without messing up each other’s work. GitHub makes it easy to share and collaborate on code with others.
  
- **Track Changes and Manage Versions:** Git helps you keep track of all the changes made to your code, so you can always go back to earlier versions if something goes wrong.
  
- **A Must-Have Skill for Developers:** Almost every company uses Git and GitHub, and knowing them is expected from developers. It’s a key skill in the tech industry.

- **Better Job Opportunities:** Employers look for developers who know how to manage code effectively, and Git/GitHub expertise can make you stand out.

learning Git and GitHub will help you work more efficiently, collaborate better, and make you job-ready in the tech world.

## Install Git & Create a GitHub Account  

**1. Install Git:**  
- Download Git from [git-scm.com](https://git-scm.com/downloads).  
- Install it with default settings.  
- Verify by running `git --version` in the terminal.  

**2. Create a GitHub Account:**  
- Go to [GitHub](https://github.com/) and sign up.  
- Verify your email and set up your profile.  

<br>

# Time to Explore Git!

### Start Learning Git from CMD  

Let’s start directly with using **Git in the Windows Command Prompt (cmd)** to manage code and track changes. By learning Git through CMD, a deeper understanding of version control can be gained at its core.  

#### **Getting Started:**  
1. **Open CMD:** Press **Win + R**, type `cmd`, and hit **Enter** to open the Command Prompt.  
2. **Check Git Installation:** Type the following command and press **Enter**:  
   ```
   git --version
   ```  
   If Git is installed, the version number will be displayed.   

3. **Next, let's configure Git using `git config`**  
This step involves setting your username and email so that Git can track your commits properly. It ensures your contributions are identified correctly in every repository.

### What is `git config`?  

`git config` is a command used to set configuration options for Git. It helps to customize your Git environment, such as setting your username, email, and other preferences that Git uses to track your activity.  

#### **Setting Username and Email**  

When using Git, each commit needs to be associated with a name and email to identify the author. You can set these details using the following commands:  

1. **Set Username:**  
   ```sh
   git config --global user.name "Your Name"
   ```  

2. **Set Email:**  
   ```sh
   git config --global user.email "your-email@example.com"
   ```  

The `--global` flag means these settings will apply to all repositories on your computer. If you want to set a different username or email for a specific repository, you can omit the `--global` flag and run the commands inside the repository folder.

#### Without Global Command for a Specific Repository
To set the username and email only for a specific repository, navigate to the repository folder and use the following commands:

1. **Set Username:**

```sh
git config user.name "Your Name"
```

2. **Set Email:**

```sh
git config user.email "your-email@example.com"
```

These settings will apply only to the current repository and will not affect other repositories on your system.

#### **Why is This Important?**  

- **Identifying Commits:** Every commit you make is tagged with your username and email, allowing others to identify who made which changes in a project.  
- **Collaboration:** It’s crucial when collaborating on projects to have accurate information about who is responsible for changes.  
- **Consistency:** Using the same username and email across all projects helps maintain consistency in your version history.  

#### **Removing Git Username and Email Configuration**  

If you need to remove or reset the username and email configuration in Git, you can do so using the following commands.  

#### **1. Remove Global Username and Email**  
To remove the globally set username and email, use:  

```sh
git config --global --unset user.name
git config --global --unset user.email
```  

This will clear the globally configured values, meaning Git will no longer associate a name and email with your commits unless set again.  

#### **2. Remove Repository-Specific Username and Email**  
If you have set a username and email for a specific repository and want to remove them, navigate to the repository folder and run:  

```sh
git config --unset user.name
git config --unset user.email
```  

This removes the username and email only for that particular repository. 

### **Create Directory and File**  

You can create a directory manually or by using the Command Prompt.  

#### **1. Creating a Directory Using Command Prompt**  

1. **Go to a Drive (if needed):**  
   - To switch to the `D:` drive, type:  
     ```sh
     D:
     ```  
   - To switch to the `C:` drive, type:  
     ```sh
     C:
     ```  

3. **Navigate to a Folder (if needed):**  
   - Example:  
     ```sh
     cd Projects
     ```  

4. **Create a New Directory:**  
   - Example:  
     ```sh
     mkdir gitPractice
     ```  

5. **Enter the Directory:**  
   - Example:  
     ```sh
     cd gitPractice
     ```  

#### **2. Creating a File Using Command Prompt** 
For Git learning, as a beginner, we start by creating a simple .txt file. After gaining experience, you can use files with any extension.


1. **Create a Text File:**  

   ```sh
   echo. > test.txt
   ```  

Now, the directory and file are ready for use.

### **Initialize Git in the Directory**

Once you have created the directory and file, you can initialize a Git repository in it using the following command:

Run the command to initialize Git:  
```sh
git init
```

This will create a `.git` folder inside the directory, marking it as a Git repository. You can confirm this by using the following command:  
```sh
dir /a
```

Now, you can start tracking changes and managing version control.

### **Three Stages of Local Repository Version Controlling**  

Git tracks files in three stages during version control:  

1. **Working Directory (Untracked Area)**  
   When a file is created or modified, it remains in the working directory. At this stage, Git does not track the file, meaning it is untracked.  

2. **Staging Area (Ready for Commit)**  
   To track changes, the file must be added to the staging area. Once added, it becomes ready for the next commit. The staging area holds changes that are prepared to be saved.  

3. **Committed (Tracked State)**  
   After staging, the file is committed to the repository. Once committed, Git starts tracking the file, saving its version history for future reference.