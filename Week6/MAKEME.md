# Homework Week 6

>[Here](https://github.com/SocialHackersCodeSchool/JavaScript/tree/master/Week6/README.md) you find the readings you have to complete before the seventh lecture.

### Step 1: Feedback

Give feedback on `step 3` of `week 5` to one of your fellow students. You should comment on Trello to do this.

### Step 2: Fix issues and API

- You'll recieve feedback from one of our teachers. Make the changes and then continue to the next step.

### Step 3: SPA :sweat_drops:
You are going to write a SPA (Single Page Application) that uses the [Github API](https://developer.github.com/guides/getting-started/). Make sure that your app uses a logical pattern just like [this codepen](http://codepen.io/Razpudding/pen/MmVpeW).

Just like last week:

Make a website that fetches (= to get) data asynchronously.

1) Create a new website with external js file

2) Add a button (e.g. 'click me') that when clicked `console.logs` 'you clicked me!'

3) Create a function that fetches from [The Github API](https://developer.github.com/v3/). For example from [this page] (https://api.github.com/orgs/SocialHackersCodeSchool/repos). For help on this check this [SO post](https://stackoverflow.com/questions/247483/http-get-request-in-javascript)

4) Display the data that you get from the Github API on your web page.

5) Now link the two together: When you click the button -> get the data from the Github API and display it on your website

Cool we are back where we left of.

6) Take a look at this:

```js
https://api.github.com/repos/SocialHackersCodeSchool/CommandLine
```

7) Make a function which takes a single argument. The function should make an Fetch request to `https://api.github.com/repos/SocialHackersCodeSchool/[SearchTerm]` where the search term will be the argument. This argument will be the input the user has given you, so make sure that when the user clicks the button you call this function with the argument. 

8) Make all the repositories link their own page in Github. Use the value of the key: `name` to make this work (hint: Github urls always look like this https://api.github.com/repos/SocialHackersCodeSchool/[repositoryName] where [repositoryName] would be replaced by the actual `name` of the repository, for example `CommandLine`). Make sure the link opens in a new tab.

- Make sure you handle user input well. That means you need to think about empty input, and input that doesn't yield any results.

So Github has this really nice documentation :octocat: :
Check these out for example
https://developer.github.com/v3/repos/collaborators/
https://developer.github.com/v3/repos/commits/

9) Extend your page with an input element. This is so the user will be able to type in text.

10) For each repository, show (in the right column) who the contributers are. You will need to use the `contributors_url` for this.

!Important
- Do not duplicate code! This is especially important for making requests since we are making multiple ones with different urls and we want to do different actions based on the call we are making. Here are some handles to get you started:
  - So write a function called `makeRequest` which accepts (at least) the following parameters: `url` and `callback`.
  - Make sure your `callback` is called when the request errors or when it sends a response (look at the documentation)
  - Your `callback` functions should accept two parameters so it can handle both errors: `err` and `response`.
  So based on your users actions (input, hovering, clicking) you want to call `makeRequest` with a different `url` and supply it with a function that handles both errors (display an error message to the user for example) and responses (render it correctly, as described below). 
 - Make your functions small and reusable (modular)! That means create separate functions to handle certain steps. 

11) GO WILD

Again, check out the Github API documentation to see what kind of magic stuff you can do with it.

The assignment is to implement something extra that is not in the assignment :scream: (nice and vague right?)

So for example, we have teams in our organization. You can find out who are in there and make a call to 'https://api.github.com/users/' + userInput (where userInput is a string typed into a search field by a user). You can show the users name, avatar image (not the link to the image!) and the number of public repos they have. Or you could make an API call to 'https://api.github.com/users/user/repos' to find out the public repo's they have. Or you can show how many people starred a specific repository. 

Anyway, endless fun and possibilities. Need inspiration, check out the Github API documentation. Oh and please make it look nice (hint: use the stuff you learned in HTML/CSS)!

__Bonus__: Write a function takes this array `['a', 'b', 'c', 'd', 'a', 'e', 'f', 'c']` and returns an array which only has unique values in it (so it removes the duplicate ones). Make it a 'smart' algorithm that could do it for every array (only strings/number). Try to make it as fast as possible!


```
How to hand in your homework:
• Upload your homework in your "sha-javascript2" Github repository. Make sure to create a new folder "week3" first. 
• Upload your homework files inside the week3 folder and write a description for this “commit”.
• Your sha-javascript2/week3 should now contain an index.html, main.css and a script.js file (and the images folder)
• Place the link to your repository folder in Trello.
```
