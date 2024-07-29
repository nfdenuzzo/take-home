# API Documentation

## Resources

This project uses the JSON Server library: [typicode/json-server](https://github.com/typicode/json-server).

### Products Routes

```
GET    /products
GET    /products/:id
POST   /products
PUT    /products/:id
PATCH  /products/:id
```

### Filtering

Use `.` to access deep properties.

```
GET /products?contract=true
GET /products?tags_like=Petrol
GET /products?id=182&id=194
GET /products?thumbnail.width=770
```

### Pagination

Use `_page` and optionally `_limit` to paginate returned data.

The `Link` header will include `first`, `prev`, `next`, and `last` links.

```
GET /products?_page=3
GET /products?_page=2&_limit=20
```

_10 items are returned by default._

### Sorting

Add `_sort` and `_order` (ascending order by default).

```
GET /products?_sort=title&_order=DESC
```

### Slicing

Add `_start` and `_end` or `_limit` (an `X-Total-Count` header is included in the response).

```
GET /products?_start=20&_end=30
```

_Works exactly like [Array.slice](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) (i.e., `_start` is inclusive and `_end` is exclusive)._

### Operators

Add `_gte` or `_lte` for getting a range.

```
GET /products?thumbnail.width_gte=1500&width_lte=2000
```

Add `_ne` to exclude a value.

```
GET /products?id_ne=1
```

Add `_like` to filter (RegExp supported).

```
GET /products?title_like=Ha
```

### Full-text Search

Add `q`.

```
GET /products?q=energy
```

---

## Important Note

You must use the [typicode/json-server](https://github.com/typicode/json-server) library for this project. Ensure you select a version that works seamlessly with your solution. Part of this challenge is to identify and use a compatible version without specific guidance on which version to use.
