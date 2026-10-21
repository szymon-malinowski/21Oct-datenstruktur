# Individual Learning Phase: Data Structures and Basic Algorithms in Node.js

## Your Goal

You are developing a small Node.js script to analyze API requests. You will work with arrays, compare simple data structures, implement a linear search, sort data using Bubble Sort, and build your own stack based on the LIFO principle.

## What You Need

- Node.js
- A code editor
- A terminal
- A project folder, e.g., `request-analyzer`
- Basic knowledge of JavaScript and how to run Node.js files with `node file.js`

## Time Schedule

- **10 minutes:** Set up the project and prepare the data basis
- **20 minutes:** Examine arrays and note simple structure comparisons
- **20 minutes:** Implement and test linear search
- **25 minutes:** Implement Bubble Sort for request durations
- **25 minutes:** Implement a Stack in JavaScript
- **20 minutes:** Consolidate everything into a small analysis script

## Basic Tasks

### Task 1:

Prepare the Data Basis
**Goal:** You create a realistic foundation for all further tasks.
**Instructions:** Create a file `requests.js` or `app.js` and create an array with at least 10 request objects. Each object should contain fields such as: `id`, `route`, `method`, `status`, `durationMs`. Use realistic values like `/users`, `/login`, `/orders`, `GET`, `POST`, status codes, and different execution times. Output the complete array to the console.
**Expected Result / Desired State:** You have a working Node.js script with an array of at least 10 request objects, which is output without errors.

### Task 2:

Arrays and Basic Structure Comparisons
**Goal:** You understand how arrays work and why a stack is useful in comparison.
**Instructions:** Extend your script with short code examples using your request array:
- add a new request
- remove the last request
- access the first and last entry
- output the number of requests

Additionally, create a short comparison in a file `notes.md` or as a comment block in your code:
- What is an array practical for?
- Why would a stack be more practical in a backend scenario?
- Name at least one example from the backend, e.g., history of last actions, undo steps, return logic, or recently processed jobs.
**Expected Result / Desired State:** You have functional code for typical array operations and a short, understandable comparison between array usage and stack usage.

### Task 3:

Linear Search for Request IDs
**Goal:** You implement a simple search function for unsorted data.
**Instructions:** Write a function `findRequestById(requests, id)` that linearly searches the array and returns the matching request. If nothing is found, a meaningful return value or an appropriate message should be output. Test the function with:
- an existing ID
- a non-existing ID

Optionally, extend the function so you can additionally search by a route, e.g., `/users`.
**Expected Result / Desired State:** You can search unsorted request data using linear search and get comprehensible results in the console.

### Task 4:

Bubble Sort for Request Durations
**Goal:** You sort data step-by-step with a simple sorting algorithm.
**Instructions:** Create a function that sorts your requests by `durationMs` in ascending order using Bubble Sort. Initially, work directly with an array of numbers or sort the request objects based on their `durationMs` value. Output the order before and after sorting.

Afterwards, add a brief assessment in `notes.md` or in the comments:
- Approximately how many comparisons are made with little data?
- Why is Bubble Sort rather impractical for large datasets?
- Does your solution require additional memory, or do you sort directly within the existing array?
**Expected Result / Desired State:** You have a working Bubble Sort implementation and can output the sorted durations or requests in ascending order.

### Task 5:

Implement Your Own Stack in JavaScript
**Goal:** You practically implement the LIFO principle.
**Instructions:** Implement your own Stack structure as a class or factory function, e.g., `Stack`. Include at least these methods:
- `push(element)`
- `pop()`
- `peek()`
- `isEmpty()`
- `size()`

Then use the stack for a small backend-related example: Store the recently processed requests on the stack. Push at least 5 requests one after another, output the top entry using `peek()`, and then remove two entries using `pop()`.
**Expected Result / Desired State:** You have your own Stack implementation that correctly works according to the LIFO principle and is tested with your request data.

### Task 6:

Consolidate Mini-Analysis Script
**Goal:** You connect data structures and algorithms in a small Node.js tool.
**Instructions:** Create a file `analyzeRequests.js` where you bring together the previous components. When started, the script should do at least the following:
- load all requests
- find a request using linear search
- sort all requests by `durationMs`
- output the 3 slowest requests
- demonstrate a stack with the most recently processed requests

Structure the code clearly with functions and meaningful console outputs.
**Expected Result / Desired State:** You have a working Node.js script that combines search, sort, and stack functionality in a realistic example.

## Extension Tasks

### Extension Task 1: Search by Status Code

**Goal:** You extend the linear search for multiple hits.
**Instructions:** Write a function `findRequestsByStatus(requests, status)` that returns all requests with a specific status code, e.g., `200`, `404`, or `500`. Output the matches clearly and also indicate if there are no matching entries.
**Expected Result / Desired State:** You can linearly find multiple matching elements in an array and display them meaningfully.

### Extension Task 2: Bubble Sort Descending or Reusable

**Goal:** You make your sorting function more flexible.
**Instructions:** Adapt your Bubble Sort function so that you can sort either in ascending or descending order. Optionally, you can also add a parameter to sort by different fields, e.g., `durationMs` or `status`.
**Expected Result / Desired State:** Your sorting is reusable and not limited to a fixed case.

### Extension Task 3: Stack for Undo of Request Markings

**Goal:** You use the stack in an even more realistic application scenario.
**Instructions:** Add a field like `reviewed: false` to your requests. Write a function that marks a request as reviewed and saves the previous state to a stack. Then implement an undo function that restores the last state.
**Expected Result / Desired State:** You use the stack meaningfully for an undo function and can roll back changes to the data.

## Important Notes

- Work in small, testable steps.
- Regularly run your script with `node filename.js`.
- Use `console.log()` or `console.table()` to visualize intermediate results.
- Pay attention to descriptive function names and clean indentation.
- If you get stuck at any point, first simplify the data or test with smaller arrays.
- Do not accidentally overwrite data when sorting or removing elements.

## Reflection Questions

- When is an array sufficient for your problem?
- When is a stack the better choice?
- What happens during a linear search if the array becomes very large?
- Why is Bubble Sort easy to understand but often unsuitable for large datasets?
- At which point in your script do you see the strongest practical relevance to a backend project?