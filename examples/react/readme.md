# FOLD Developer Interview Project - todomvc
## Sunit Mody (2021)

## Table of Contents
1. [Project Description](#description)
2. [Project Template Link](#link)
3. [Getting Started](#getting)
4. [Implemented Feature](#feature)
5. [Highlights](#highlights)
6. [Possible areas of improvement](#improvements)
7. [Technologies](#techs)
8. [Miscellaneous](#misc)

<a name="description"/>

## Project Description
- This project is a modification to an existing todoMVC implementation created using React

<a name="link"/>

## Project Template Link
- The orignal repo that I modified:
  -  https://github.com/tastejs/todomvc/tree/gh-pages/examples/react
- Original application hosted online:
  - https://todomvc.com/examples/react/#/

<a name="getting"/>

## Getting Started
- Fork and clone repo to your local enviornment

- From within the repo root directory
```
$ npm install
```

- From within the root directory of the React sub-repo (~/todomvc/examples/react)
```
$ npm install
```

- Start gulp server on port 8000
```
$ npm start
```

- View app locally in browser
```
http://localhost:8000/examples/react/#/
```

<a name="feature"/>

## Implemented Feature
- The feature I added was the functionality to add one or multiple space separated tags to each todo item that is created. The tags are visible next to each listed todo item. The user is able to filter through the todos and display them by selecting one or multiple tags. The user can also remove an already selected tag, for filtering, by clicking on it again. Lastly, the user can click "Clear tags filter" to completely remove all tag filters.

### Original
<img src="readme_images/original_todo.png" width="600">

### After tag feature added
<img src="readme_images/tag_feature.png" width="600">

<a name="highlights"/>

## Highlights
- Added CSS styling (including flex-box) to make tags easily visible. Also added a different color hover highlighting of tags to differentiate from active vs completed filters.

- Utilized array methods (some of which are higher-order functions) such as .map, .filter, .flat and .some to modify arrays to help with state management.

- Managed filtering of todos by tags using a click-handler to modify state. This is different than the existing filtering logic of active vs completed todos which uses the URL's endpoint and routing to modify state.

- Implemented logic to prevent repeated tags from appearing in the footer and for todos without tags to not cause erroneous HTML elements to be created in the footer or next to the todo item.

<a name="improvements"/>

## Possible areas of improvement

- Update React and JS syntax to ES6 and/or use React Hooks

- Add the functionality to edit or remove existing tags

- Highlight selected tags so it's easy to see which tags are currently being used to filter the todos with

- Create a separate component for "tag" and maybe "tagInput" for better separation of concerns

- Clean up styling to be able to handle numerous tags without cluttering the footer component

- Change tags filter logic from "union" to "intersection"

<a name="techs"/>

## Technologies

Highlighted Technologies:
- React
- Gulp
- Javascript

<a name="misc"/>

## Miscellaneous (Changes made to original repo to get it to work)
- Installed gulp command line interface (npm install --global gulp-cli)
- Updated devDependencies in root directory to "gulp": "^4.0.0",
- Updated gulp to latest version 4.0.2
- Modified gulpfile in root directory to use gulp.series() (modfication required because old code was deprecated)
- CSS modified at ~/react/node_modules/todomvc-app-css/index.css
- If any errors encountered, try localStorage.clear() in the console. State data is being stored locally in the broswer and may need to be cleared.