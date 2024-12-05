# Movies list - Fetch movies

Implementув the `FindMovie` component to load movies from [OMDb API](http://www.omdbapi.com/)

1. When a user enters a title and submits the form, send a request to `https://www.omdbapi.com/?apikey=[yourkey]&t=[title]`;
   - use the `getMovie` method from the `api.ts`;
1. The submit button should be disabled when the title field is empty;
1. Show a spinner on the submit button while waiting for the respose;
   - use `is-loading` class;
   - loading should be finished in any case (use `finally`);
1. If a movie is not found show an error message below the input;
   - hide it after changing the title;
1. If a movie is found show the preview as a `MovieCard` and the add button;
   - the API return `MovieData` or `ReposnseError` (see the `types`)
   - don't forget to normalize received `MovieData`
   - use [the deafult picture](https://via.placeholder.com/360x270.png?text=no%20preview) if the found movie has no poster.
1. The add button should **add** the movie to the list, **clear** the form and **remove** the preview;
1. Don't add a movie to the list twice (compare by `imdbId`), just clear the data;

## Demo Links

- [DEMO LINK](https://AndriiZakharenko.github.io/react_movies-list-fetch-movies/)
