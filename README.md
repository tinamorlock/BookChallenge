# BookChallenge
Python/Django web app that uses CRUD, web scraping, JavaScript, and APIs to create a collection of tools for book lovers. App was part of a bigger project that had a directory of apps, so this repository does not include the full code to run the web application. However, you can find all the code I wrote in my portion in this README file.
## Features
* Homepage that includes quotes from famous authors and YouTube videos about reading and books
* Ability for user to add book to their library database
* Ability for user to edit books in their library and delete them
* Display all entries in the book database
* JavaScript alarm that works as a reading timer
* Implementation of NY Times API to display NY Times Bestsellers
* Index of individual poems to read that are populated through web/data scraping
* The ability to add favorite poems to a database to save for reading later
## Custom CSS
```
/* whole site styling */

body {
    font-family: Helvetica, Arial, sans-serif;
    background-color: black;
    color: white;
}



/* top nav styling */

.book-nav {
    background-color: #377E9F;
    overflow: hidden;
    top: 0;
    left: 0;
    position: sticky;
    width: 100%;
}

.book-nav a {
    float: left;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
}

.book-nav a:hover {
    background-color: #CE3243;
    color: white;
}

.book-nav:after {
    content: "";
    clear: both;
}


/* footer styling */

.book-footer {
    background-color: #377E9F;
    width: 100%;
    color: white;
    position: fixed;
    left: 0;
    bottom: 0;
    text-align: center;
    padding: 8px;
}

/* image styling */

.center-image {
    display: block;
    margin-left: auto;
    margin-right: auto;
}

.full-width {
    width: 100%;
}

.collage-smaller {
    width: 75%;
}

/* styling for the form that adds a book into the DB */

.book-form {
    background-color: #CBDFDA;
    width: 25%;
    margin-left: auto;
    margin-right: auto;
    padding: 20px;
    border: 2px black dashed;
    border-radius: 3px;
    margin-top: 25px;
    color: black;
}

.book-form input {
    width: 35%;
}

.book-heading-1 {
    background-color: black;
    padding: 2px;
    border: 1px solid black;
    border-radius: 5px;
    color: #CBDFDA;
    text-align: center;
}

/* adding styles for logo */

.logo-container {
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 20px;
}
.logo-container img {
    width: 10%;
 }

/* text styles */

.text-centered {
    text-align: center;
}

/* styling for tables that display DB items */

.TC-row {
    margin-top: 25px;
    margin-left: 25%;
    margin-right: -5px;
}

.TC-column {
    float: left;
    width: 20%;
    padding: 5px;
}

.TC-column-2 {
    float: left;
    width: 65%;
    padding: 5px;
}

.TC-column-3 {
    float: left;
    width: 40%;
    padding: 5px;
}

td.poetry-cell, th.poetry-cell {
    height: 50px;
}

.bestsellers-row {
    margin-top: 25px;
    margin-right: -5px;
    margin-left: 35%;
}
.bestsellers-column {
    float: left;
    width: 25%;
    padding: 5px;
}

.bestsellers-row::after {
    content: "";
    clear: both;
    display: table;
}

.TC-row::after {
    content: "";
    clear: both;
    display: table;
}

table {
    border-collapse: collapse;
    border-spacing: 0;
    width: 100%;
    border: 2px solid #CE3243;
    border-radius: 3px;
}

th, td {
    text-align: left;
    padding: 16px;
    height: 100px;
}

th {
    font-size: 56px;
}

tr:nth-child(even) {
    background-color: #CBDFDA;
    color: black;
}

tr:nth-child(even) a {
    color: #377E9F;
}

.no-border {
    border: none;
}

/* styling for link buttons */

.link-button {
    background-color: #CE3243;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 4px;
}

a {
    color: white;
}

.turq-link {
    color: #377E9F;
}

.book-button {
    background-color: black;
    color: #CBDFDA;
    font-size: 24px;
}

.book-button-red {
    background-color: #CE3243;
    color: white;
    font-size: 32px;
}

.button-group {
    display: block;
    margin-left: 40%;
    margin-top: 20px;
}

.book-title {
    color: #CE3243;
}

.spacer {
    margin-top: 25px;
    display: block;
}

/* styles for reading timers */

/* buttons */
.clock-button {
  cursor: pointer;
  margin: 0 5px;
  padding: 10px 30px;
  background: transparent;
  border: 1px solid #CE3243;
  border-radius: 8px;
  outline: 0;
  color: black;
  transition: all ease 300ms;
}
.clock-button:hover {
  color: #333;
  background: #fff;
}

/* center content vertically and horizontally */
.clock-table {
  display: table;
  width: 100%;
  height: 100%;
}
.clock-cell {
  display: table-cell;
  vertical-align: middle;
  cursor: default;
}

/* variable misc classes */
.hide {
  display: none;
}

.reading-timer {
    background: #CBDFDA;
    text-align: center;
    margin-top: 25px;
    width: 30%;
    display: block;
    margin-left: auto;
    margin-right: auto;
    border: 2px dashed #CE3243;
    border-radius: 3px;
    color: black;
}

/* quotes container for home page */

.quote-outer {
    background-color: #CBDFDA;
    color: black;
    width: 90%;
    display: block;
    margin-left: auto;
    margin-right: auto;
    padding: 10px;
    border: 2px solid #CE3243;
}

.quote-row {

}

.quote-row::after {
    content: "";
    clear: both;
    display: table;    /* might need to remove this, as this isn't a table? */
}

.quote-column {
    width: 30%;
    padding: 5px;
    background-color: black;
    border: 1px solid black;
    border-radius: 5px;
    float: left;
    margin-left: 25px;
}

.quote-content {
    color: #CBDFDA;
}

.quote-author {
    color: black;
    text-align: center;
    background-color: #CBDFDA;
    width: 50%;
    margin-top: 15px;
    margin-left: 50%;
    border: 1px solid #CBDFDA;
    border-radius: 10px;
}

/* quotes don't display on a smaller screen.
    My screen is pretty large, so I want to make sure it
    displays right for everyone who sees it. */

@media (max-width: 1024px) {
    .quote-outer {
        display: none;
    }
}

/* home page animation */


#container {
  color:#999;
  text-transform: uppercase;
  font-size:36px;
  font-weight:bold;
  padding-top:50px;
  width:100%;
  bottom:45%;
  display:block;
  margin-left: 45%;
  margin-bottom: 40px;
}

#flip {
  height:50px;
  overflow:hidden;
}

#flip > div > div {
  color:#fff;
  padding:4px 12px;
  height:45px;
  margin-bottom:45px;
  display:inline-block;
}

#flip div:first-child {
  animation: show 5s linear infinite;
}

#flip div div {
  background:#377E9F;
}
#flip div:first-child div {
  background:#CE3243;
}
#flip div:last-child div {
  background: white;
  color: black;
}

@keyframes show {
  0% {margin-top:-270px;}
  5% {margin-top:-180px;}
  33% {margin-top:-180px;}
  38% {margin-top:-90px;}
  66% {margin-top:-90px;}
  71% {margin-top:0px;}
  99.99% {margin-top:0px;}
  100% {margin-top:-270px;}
}

.YT-row {
    margin-top: 25px;
    margin-left: 15%;
}

.YT-column {
    float: left;
    width: 40%;
    padding: 5px;
}

.YT-row::after {
    content: "";
    clear: both;
    display: table;
}

.YT-column-next {
    float: left;
    width: 40%;
    padding: 5px;
    margin-left: 100px;
}

.center-poem {
    display: block;
    text-align: center;
    }
```
