# Episode queries

This directory contains GraphQL queries for fetching episode data from the API.

Files
- `episode-page-1.graphql` - Parameterized query to fetch an episode by ID.
- `episode-id-1.graphql` - Example query that requests episode with id `1`.

Usage

Query to fetch a specific episode by ID (parameterized):

```graphql
query GetEpisodeById($id: ID!) {
  episode(id: $id) {
    id
    name
    air_date
    episode
  }
}
```

Example variables:

```json
{
  "id": "1"
}
```

Example (hardcoded id):

```graphql
query {
  episode(id: 1) {
    id
    name
    air_date
    episode
  }
}
```
