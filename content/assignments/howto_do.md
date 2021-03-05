# Homework guidelines

## Starting homework

1. **Click on the assignment link in coursesite.** When you follow the link and accept the assignment, GitHub will create a repo for you. The repo will be a private repo (only you, me, and the TA can see it) under the LeDataSciFi organization on GitHub. 
1. The repo will contain instructions and a rubric, and possibly starter code/data.
2. Clone the repo to your local machine using GitHub desktop and follow the instructions. 

## Working on assignments / projects / taking notes 

```{tip} 
**Fetch early, commit frequently, push often!**

This habit will help you avoid disasters, so that you get the positive features of Github without the headaches.

```

````{dropdown} 1. Make your coffee, open Github Desktop, and **FETCH** the project you'll work on. 
1. Change the "current repository" to the assignment you want to work on (or project, or your notes repo, etc.)
1. Click "Fetch origin" to download any changes from the master repo on the Github servers. This is important, because if someone else changed the files while you were sleeping, you'll get the most updated files to work on. 
1. Start your work on your computer. 

![](https://media.giphy.com/media/xUOrwpPFzqDh48XEek/giphy.gif)

```{warning}
If you don't "fetch" before you start, it's becomes easier to change a file someone else changed differently, creating a conflict. When this happens, you have to resolve the conflicting files before moving on. 
```

````

````{dropdown} 2. **"COMMIT" FREQUENTLY** (say every 30 minutes or so, but depends on the team/task): 
- Save the files you're working on. (Just like you would while working on a Powerpoint or Word document.) 
- When you save the file, Github Desktop (GHD) will notice it has been changed. 
- Go to GDH. Notice that your file is listed as a "changed" file. 
- **Describe those changes in the "Summary" and (optionally) "Description" boxes, and click the blue "Commit" button**. 
- Try to do this every time you save your files! It will make rolling back changes easier. 
- **Do this early and often**

```{panels}
![](https://media.giphy.com/media/l4KhSYN6hQ7Y0FZS0/giphy.gif)
---
![](https://media.giphy.com/media/dxITs87fTAxTncZ6WL/giphy.gif)
```
````

```{dropdown} 3. **"PUSH" OFTEN, but probably less than you commit** (say every 60-90 minutes or so, but depends on the team/task): 
- Push your changes to the cloud by clicking the blue "push" button in GHD. 
- Now, you've got an up-to-date backup and teammates can see the changes and work with the latest files.
- GHD will warn you if someone else made a change in the meantime. If this happens, click "fetch" to download what they did. If there is a conflict between your work and your teammate's, you'll have to resolve it. 

![](https://i.imgflip.com/4m0jf6.jpg)

```

```{tip} 
**I call these three steps our "GitHub workflow".**
```

## Submitting assignments 

Submission is easy: Whatever is in your assignment repo (the online version, not your computer!!!) at the deadline is what will be graded. 

```{warning}
Again: Whatever is in your assignment repo (the online version, not your computer!!!) at the deadline is what will be graded.
```

```{warning}
Shortly after the deadline, GitHub will automatically stop you from pushing edits to the repo! So commit and push your changes often, and do not wait until minutes before the deadline. 
```

Your graders will download your repo on their computer, try to run your code, and evaluate it for accuracy and quality, based on the rubric (each assignment has a different rubric). 

## Tips for better grades (+ workproduct + repos)

```{admonition} TODO prof - this is too long. simplify
```

```{dropdown}  **TIP #1:** Check out the rubric for the assignment
Each assignment has different grading criterion, which you'll see when when the assignment is posted. For a good summary, see the [guidelines for peer review page](howto_review). 

Generically and briefly, I'll say the important themes are:
- reproducibility (Your peers should be able to download the folder to their computer and execute the main analysis file and receive back the same results you generated)
- organization of the repo (can an outsider discern what is going on?)
- the README.md file, which should describe the repo to readers 
- the main analysis file. More on this in the next Q...
```




```{dropdown}  **TIP #2:** Before you push what you think are your final changes to the master repo...
1. Delete all temporary files you generated, along with any outputs, and
2. rerun the analysis/code as though you just downloaded. 

This will clean up your folder for viewers (yay, professional work product!) and is a first pass at finding out if your code "works from scratch".

Did it work? If not, then the code is not reproducible. Probably, you referenced a temporary file you created outside of the flow of the code, or accidentally put an input file in the temporary file folder. Whoops! Fix it!
```



```{dropdown}  **TIP #3:** After you push what you think are your final changes to the master repo...
1. Go to the repo _**online**_. This is what your reviewers will see. The process of writing code often creates little files (like `.ipynb_checkpoints`) that you don't want in the online repo, but that you can't or don't want to delete locally. The usual solution is to add them to gitignore and purge them from the master repo. (This is easy, and I'll describe how to do it elsewhere.)
2. **A 100% solution**: Download it to your computer (click the green button, then download the zip file) **to a different spot** (say a temporary folder on your desktop), and run the analysis again, there. 

Did it work? If not, then the code is not reproducible outside the directory you built it in. 

Why did it fail? Probably, the code included absolute path references like "C:\Users\DonBowen\Documents\project1\code\extra_function.py". These are bad, because they only work on my computer. (You probably won't have "DonBowen" as a folder anywhere on your computer, I hope!)  

Use relative path references instead. For example, if `main_analysis.py` uses `extra_function.py`, and `main_analysis.py` is in the "project1" folder, then "code/extra_function.py" will find the function on any computer. 
```




```{dropdown}  **TIP #4:** Make it easy for others to see the source code that executes the analysis as well as the report. 
The biggies:
1. The README.md in the main directory is what they will see first when they open it. Make it professional and helpful!  GitHub can format "Markdown" nicely, with headers, links, media, and more and will show visitors this. Create annotated links to documents graders need to access. You should point them to your main Jupyter file, which GitHub will also render!
2. Make sure your final analysis code shows outputs _when viewed online_! This will help them grade faster (and faster graders are nicer graders).
```


```{dropdown}  **TIP #5:** Make it easy for others to run your code.
- At the top of the code, load all packages you need
- Under that, list parameters a user would set (you obviously choose these during your analysis, but it's nice to see quickly and wholly)
- Under that, import external files. This makes it easy for someone to see which data files are required and edit the paths if necessary. Even though I said absolute path references are bad above, there are situations where you might not keep data in the repo itself. (For example: Huge data files or sensitive data subject to privacy issues.) When this is the case and you have to use absolute path references, you want those at the top of your code so people see them!
- Again, see tip #3 above.
```


```{dropdown}  **TIP #6:** Make your work product (especially tables and figures) pretty. 
- Use good design concepts that we discuss early in the semester for figures and tables.
- I google "markdown cheat sheet" often (sometimes with "github" or "jupyter" added to it depending on what I'm writing). [This is a good start cheat sheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf) and there is so much good stuff online. 
```


