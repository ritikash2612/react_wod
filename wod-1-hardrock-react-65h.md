---
title: "WOD: Hard Rock Cafe (React Version)"
published: false
morea_id: wod-hardrock-65h
morea_type: experience
morea_summary: "Test your knowledge of Semantic UI and React" 
morea_sort_order: 1
morea_labels:
---

# WOD: Hard Rock Cafe (React Version)

[The Honolulu Hard Rock Cafe](http://www.hardrock.com/cafes/honolulu/) is a popular local music venue. For this WOD, you will create a web page using React and Semantic UI inspired by their home page. When completed, it should look like this (click on image to see full size):

{% include medium-img.html url="wod-1-hardrock-react-2.png" %}

Note that you will find your code from [Experience Island Snow React](experience-islandsnow-react.html) to be very helpful.

Here are the steps:

## Task 0: Download the Semantic UI mockup

Please download the [Semantic UI HardRock Mockup Source](wod-1-hardrock-semantic.zip) zip file. Uncompress it, and double click on the index.html file to display the mockup of the HardRock home page. Your task is to convert this Semantic UI code to React for this WOD.

## Task 1: Set up your development environment.

Create a private GitHub repo called hardrock-react and initialize it with a README. 

Clone it to your local workspace (preferably using GitHub Desktop).

Create an IntelliJ IDEA project called "hardrock-react" that points to your local repo.

Create a .gitignore directory, and ignore `node_modules`, `*.iml` and `.idea`. 
 
## Task 2: Create your skeleton HardRock React app.

Change directory into hardrock-react/ and invoke `create-react-app my-app`.  (This may take a few minutes.)

Change directory into my-app/.

Install Semantic UI by typing `npm install semantic-ui-react semantic-ui-css --save`

Remove all the files in the src/ directory (`rm -f src/*`)
   
Copy the style.css file from your downloaded HardRock mockup source code into the src/ directory.

Create an index.js file with the following contents:

```
import React from 'react';
import ReactDOM from 'react-dom';
import './style.css';
import 'semantic-ui-css/semantic.min.css';
import { Container, Header } from 'semantic-ui-react';

class HardRock extends React.Component {

  render() {
    return (
        <Container textAlign="center">
          <Header as='h1'>HardRock!</Header>
        </Container>
    );
  }
}

ReactDOM.render(<HardRock/>, document.getElementById('root'));
```

(You can switch to JSX if IntelliJ asks. Also, you can disable ESLint for this week.)

Now run `npm start` in your shell. If all goes according to plan, you should see the following appear at http://localhost:3000:

{% include medium-img.html url="wod-1-hardrock-react-1.png" %}

## Task 4: Build the page

Take a look at the mockup's index.html file. You can see that the home page consists of three sections:

  1. A top menu (containing the hardrock logo on the left, and menu items on the right).
  2. A middle section (containing a full-width photo)
  3. A footer containing two centered rows.
  
Similar to the [Island Snow with React experience](experience-island-snow-react.html), create three React components, one for each section of the site. 

## Hint: How to provide inline styles in the top menu

Getting the top menu items to display correctly requires using React's "inline styles".  In case you haven't seen this before, here's a partial implementation of the top menu to show you how to do it:

```
class TopMenu extends React.Component {
  render() {
    const itemStyle = { color: "#ccc", fontSize: "22px" };
    return (
        <Menu className="topmenu">
            <Menu.Item>(Logo goes here)</Menu.Item>
            <Menu.Item style={itemStyle} position="right">CAFES</Menu.Item>
            <Menu.Item style={itemStyle}>HOTELS</Menu.Item>
        </Menu>
    )
  }
}
```

## Task 5: Finish

When you can preview your application and it looks equivalent to the screen image above, commit and push your repo to GitHub.
  
Check to make sure it is present on GitHub.

Raise your hand to indicate you are done with this WOD.

{% include wod-times.html Rx="<20 min" Av="20-40min" Sd="40-60 min" DNF="60+ min" %}

### Submission instructions

{% include wod-submission-github.html assignment="React WOD" %}

{% include goo.gl.html url="" %}










