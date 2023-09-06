# odin-recipes
Recipes Website Project
1 - Setting up Github's repository
    Github is a remote Git repository hosting service. It allows developers to manage their code and do version control using Git. It makes collaboration a lot easier and it protects us from having only one local access to our code. 

    - Create a new repository (Public)
        - Add a README.md file
        - Copy the SSH key

    - Terminal: inside repository folder, use command git clone followed by the repo's SSH key
        - To verify use: git remote -v

    - Edit README.md file with project description
        - To open from Terminal code .
        - Edit and save
    
    - Once it's done, add README.md to staging area (git add README.md)
    - Next, commit files from staging area
        git commit ENTER should open Text Editor to write a descriptive commit message

    Writing a commit message
        - Separate subject from body with a blank line
        - Limit the subject line to 50 characters
        - Capitalize the subject line
        - Do not end the subject line with a period
        - Use the imperative mood in the subject line
        - Wrap the body at 72 characters
        - Use the body to explain what and why vs. 
        
        When writing code, it’s considered best practice to commit early and often. Commit every time you have a meaningful change in the code. This will create a timeline of your progress and show that your finished code didn’t appear out of nowhere.

    - Push it live: git push origin main
