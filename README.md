# odin-recipes
Recipes Website Project

Setting up Github's repository
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

HTML

Starting the document - Homepage = index.html
    <!DOCTYPE html>
    <html>
     <head>
        <meta charset="utf-8">
        <title>Odin Recipes</title>

     </head>
     <body>
     Headings (h1/2/3/4/5), paragraphs (p), lists (ul = unordered / ol = ordered), images (img src + alt) and links (a href + text for clicking).
     <div> is an empty container that usually groups sections of the website.
     </body>
     </html>

CSS - SELECTORS
    selector {property: value}
     
    Selector is the HTML element that's being selected for the CSS rules to be applied.
     - Universal selector
        * {
            color:purple;
        }

    - Type selector: this will select all the elements that equals <div>
        div {
            color: white;
        }

    - Class selector: classes can be used on multiple elemtents. Divs can be sorted in classes and all elements with a given class can have the same CSS applied. One element can also have more than one class. 
        HTML: <div class="alert-text severe-text">Please...</div>
        CSS:
        .alert-text {
            color: red;
        }

    - ID selector: similar to classes in many ways BUT an element can only have one ID. This should be used sparingly, usually classes will suffice. 
        HTML: <div id="title">Main Thing</div>
        CSS
        #title {
            background-color: red;
        } 
    
    - The grouping selector: groups of elements might have similarities between them and this is a way of cutting down on repetition.

        INSTEAD OF THIS:
        .read {
            color: white;
            background-color: black;
            /* several unique declarations */
        }
        .unread {
            color: white;
            background-color: black;
            /* several unique declarations */
        }

        Group the similarities and separate the unique declarations.

        .read,
        .unread {
            color: white;
            background-color: black;
        }
        .read {
            /* several unique declarations */
        }
        .unread {
            /* several unique declarations */
        }

    - Chaining selectors: What .subsection.header does is it selects any element that has both the subsection and header classes.
        .subsection.header {
            color: red;
        }
    
    - Descendant combinator: Combine multiple selectors that have a relationship with one another by grouping or chaining. There are other types of combinators to explore later. Example .ancestor .contents (with space, different from chaining), this means it will be applied to any contents div that is nested inside an ancestor div. 

CSS - MAIN PROPERTIES
    color / background-color
    #1100ff
    rgb(100, 0, 127)
    hsl(15, 82%, 56%)

    Typography
    font-family: "Times New Roman", sans-serif; (if a browser cannot find the first one it will go on the second)
    font-size: 22px
    font-weight: bold (or number 100-900)
    text-align: center

    Image height and width
        img {
            height: auto;
            width: 500px;
        }

Adding CSS to an HTML file

    - External CSS: most common and cleaner way of working. It will link the files in the <head> part of the HTML with: <link rel="stylesheet" href="styles.css" />
    - Internal CSS: can be useful for anything unique styles to a single page but the HTML file might end up pretty big. Should be added in the <head> with <style> </style>
    - Inline CSS: <div style="color: white; background-color: black;">...</div> We don't need selectors because it's directly applied to this specific div. 
        - Not usually recommended because it can get messy and cause a lot of unnecessary repetition.
        - This method overrides the other 2 methods, which can have its advantages but also generate unexpected results.
    
CSS - The Cascade
This determines which rule gets applied to the HTML based on different factors (including browser) and hierarchy of CSS declarations.

More specific declarations > less specific ones (i.e. Inline styles over internal/external)

Selectors specificity will be the tie-breaker in case of conflicting declarations being applied to the same element. 
    - ID = most specific
    - Class = beats type selectors
    - Type

If a declaration has more selectors, it's more specific so it takes precedent over less specific ones.







 
    







