<div align="center">
  <h1>kuryana</h1>

  <p>A simple MyDramaList.com scraper api.</p>
  <p>This scrapes on the go so it might be slow.</p>

  <h4>THIS SERVICE IS ONLY CREATED TO SATISFY THE NEED FOR AN API FOR [MYDRAMALIST.COM](https://mydramalist.com). THIS WILL BE STOPPED ONCE AN OFFICIAL API WILL BE RELEASED.</h4>

</div>

## Deployment

### [Vercel](https://github.com/tbdsux/kuryana/tree/deploy/vercel)

Make sure to set `deploy/vercel` as the branch.

## API Use

- [Search for dramas](https://kuryana.vercel.app/search/q/)

```
https://kuryana.vercel.app/search/q/{yourquery}
```

- [Get DRAMA Info](https://kuryana.vercel.app/id/)

```
https://kuryana.vercel.app/id/{mydramalist-slug}
```

- [Get DRAMA Cast](https://kuryana.vercel.app/id/{id}/cast)

```
https://kuryana.vercel.app/id/{mydramalist-slug}/cast
```

- [Get DRAMA Reviews](https://kuryana.vercel.app/id/{id}/reviews)

```
https://kuryana.vercel.app/id/{mydramalist-slug}/reviews
```

- [Get Person(People) Info](https://kuryana.vercel.app/people/)

```
https://kuryana.vercel.app/people/{people-id}
```

- [Get seasonal drama](https://kuryana.vercel.app/seasonal/)

```
https://kuryana.vercel.app/seasonal/{year}/{quarter}
```

- [Get Lists](https://kuryana.vercel.app/list/)

```
https://kuryana.vercel.app/list/{id}
```

- [Get User Dramalist](https://kuryana.vercel.app/dramalist/)

```
https://kuryana.vercel.app/dramalist/{user_id}
```

### Error Messages

```js
// mainly on all endpoints except `search`
// sample: /list/unknown-random-id
{
  "code": 400,
  "error": true,
  "description": {
    "title": "This list is private.",
    "info": "You can see this page because the URL you are accessing cannot be found."
  }
}
```

```js
// could also be this (only on `/search`) endpoint
{
  "error": true,
  "code": 404,
  "description": "404 Not Found"
}
```

## Development

- Minimum Python Version : `3.12`,

- Make sure `uv` is installed in your machine, [more details](https://docs.astral.sh/uv/getting-started/installation/)

- Sync project dependencies

  ```sh
  uv sync
  ```

### Dev Server

Start development server.

```sh
uv run fastapi dev
```

[FastAPI CLI] (https://fastapi.tiangolo.com/fastapi-cli/)

## NOTE

All Requests and SCRAPED Datas are not cached by Vercel or the API itself.

#### &copy; TheBoringDude
