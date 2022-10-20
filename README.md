# Guide-for-uplode-big-files-25mb-

1. Download and Install "git fast version control"

    URL: https://git-scm.com/downloads
2. Download and install "Git Large File Storage"

    URL: https://git-lfs.github.com/

3. Click on Search icon in Windows desktop ( on the left down corner) and search for Command Prompt

4. Type:
     git lfs install
6. Type inside the brackets your file path: 

     cd "C:\Users\Desktop\DataFiles"

8. Type inside the brackets your a file name with a file type after the dot:

    git lfs track "filename.csv"

7. Type one after another:

    git add .gitattributes
    git add file.psd
    git commit -m "Add design file"
    git push origin master
    
 Error handling:

 1. fatal: ‘origin’ does not appear to be a git repository

    Answer: 

    --- copy the URL link of your repository from the Github site – 
    --- click on Code tab > copy the HTTPS URL
    --- Type > Enter > Type: 
           -- git remote add origin "HTTPS_URL"
           --  git push origin master
            
 2. “! [rejected]        master -> master (fetch first)

     Answer:
     
        First type this:
            git fetch origin master
            git merge  master
	
	Then, type this:
	
            git fetch origin master:tmp
            git rebase tmp
            git push origin HEAD:master
            git branch -D tmp



 
