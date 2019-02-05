# Code Analysis

See comments in `index.html` for instructions.

## Run

Open `index.html` in Google Chrome.

## Style Guide

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally
- Consider starting the commit message with an applicable emoji:
  - **Improvements**
    - :art: `:art:` when improving the format/structure of the code
    - :fire: `:fire:` when removing code or files
    - :tada: `:tada:` when adding a feature
    - :goat: `:goat:` when improving performance
  - **Misc**
    - :memo: `:memo:` when writing docs
  - **Dependencies**
    - :arrow_up: `:arrow_up:` when upgrading dependencies
    - :arrow_down: `:arrow_down:` when downgrading dependencies

### React Styles

- Always favor stateless components

### My Thoughts

- I like a separation of concerns so I moved the css and javascript from the html to their own files.
- noticed the sortByLastName wasn't actually sorting by the the last name so I fixed that.
- Made the search a little more intuitive so you don't need an exact match with capitalization.
- I like the data transformation functions being separate functions for reusability, like sort by first and last names, but the search function looks like will only ever be called with the search function and could be okay in the component _onSearch_ if no other feature were going to be added.
- I would have a build step as there seems to be a bit of extra code compared to a version that uses a compiler _React.createElement(Thumbnail, { src: getImageUrl(props.person) })_
- I would split the createClass function for the list items into its own file
