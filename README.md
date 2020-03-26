# One Pager Tutorial

This is a tutorial on how to build a simple one pager website using vanilla html css and javascript.

## Setup

1. make sure you are in the right folder --> `cd` into the Developer folder
2. clone the github repository you want --> `git clone <url-project>`
3. now open the project in VSC --> `code -r <project-name>`
4. add a second remote to your own version of the repository. Go to github and create a repository with the name <_one-pager_>, copy the URL and then add it to this repository as a second remote:

`git remote add my-github https:/github.com/my-user-name/one-pager.git`

5. Now you can push your master branch like this and set it up as an upstream:

`git push -u my-github master`

6. create a branch called setup and checkout this branch

`git checkout -b setup`

7. Create the following file structure using `touch` and `mkdir`

```
/index.html
/style.css
/README.md
/LICENSE
```

8. Add the default boiler plate to `index.html` and link `style.css` into your `<head>` tag.

```html
<link rel="stylesheet" href="style.css" />
```

9. change the title inside the head tag of the page

```htlm
<title>One Pager</title>
```

10. We'll be using two external style sheets in the project. One is to include a font from google fonts, the other is an icon font called font awesome. Insert these two links into the head of the document:

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.12.1/css/all.min.css"
/>
<link
  href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap"
  rel="stylesheet"
/>
```

11. Choose a license from https://choosealicense.com/ and insert it into the LICENSE file.

12. Use the Readme file to write a tutorial on _how to create a one pager template_.

**Update it before each commit and with every step of the project. Use your own words and use it as an opportunity to keep track of the stepping stones you encounter and how you overcame them.**

13. Create a git commit using `git add` and `git commit.`

14. Now the setup branch is ready to be merged. First checkout the master branch. Then run the merge command with the `setup` branch as an argument to perform the merge. Which kind of merge is this? Fast-forward or Three-way?

```
git checkout master
git merge setup
```

15. Push both the master and the setup branch to github. We'll push our feature branches so you can later jump through the interesting checkpoints.

```
git push
git push -u my-github setup
```

## HTML Structur

1. Before you start create a new branch and check it out

```html
git checkout -b html
```

2. First step is to create the first level of structure. Create a `<header>` `<main>` and `<footer>` tag inside the body

```html
<body>
  <header></header>
  <main></main>
  <footer></footer>
</body>
```

3. create sections within `<main>` tag and use the class names ```banner```   ```about```  ```elements``` ```showcase``` and ```contact```

- Banner
- About
- Elements
- Showcase
- Contact

Each of them is a `<section>` tag which contains an inner `<div>` which has the class `section-inner-container`.
Inside the inner container we create another div and give it the class for the individual section. To later be able to link to individual sections, we give each section also an id. We put it at the tag, so the scroll doesn't scroll to far, but actually keeps the margin above the inner-container visible.

```html
<section id="banner">
  <div class="section-inner-container">
    <div class="banner">
      This is where the content for the section will go
    </div>
  </div>
</section>
```
with the following comand you create 5 identical master-templats for the ```section``` with the inner ```div``` including *id (#)* and *class (.)*
```
(section#banner>div.section-inner-container>div.banner)*5
```

### Banner
- content: 
    - heading 
    - a paragraph and 
    - a link. 
    Notice how the anchor is linking to an id we have created in the previous step: href="#contact"

```html
<h1>How to build a solid One Pager</h1>
<p>
  Every good one pager starts with a big headline. <br />
  And a subtitle maybe.
</p>
<a href="#contact">Get in touch</a>
```
Add the class btn short for button to the anchor, because this link stands on its own and is not an inline part of a text paragraph.

### About

### Elements

### Showcase

### Contact

## Styling

### Reset
