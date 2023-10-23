---
title: Entries in folder xx
---

You can use the `starts_with` parameter to load entries that are in a specific folder. This is useful if you create your articles in an `articles/` folder, `products/` in a products folder.

| Slug | Description |
|--|--|
| `?starts_with=products/` | all entries in folder `products` |
| `?starts_with=de/products/` | all entries with `de` values in translatable fields in folder `products` |
| `?starts_with=articles/` | all entries in folder `articles` |

* If you have a nested folder you can use **UnderLine** to go through the path for example
  ?starts_with=products_cloths| all entries in folder cloths child of products

;examplearea

Example Request

<RequestExample url="https://api.storyblok.com/v2/cdn/stories/?starts_with=products/&token=ask9soUkv02QqbZgmZdeDAtt"></RequestExample>

Example Response

```json
{
  "stories": [
    {
      "name": "Spaceship",
      "lang": "de",
      "created_at": "2018-12-10T17:51:25.161Z",
      "published_at": "2018-12-10T18:27:28.137Z",
      "id": 461935,
      "uuid": "14d950c6-0a8f-4088-98e3-73efced9ff6d",
      "content": {
        "_uid": "00b45e23-5dc5-4398-9b34-e87ae4ed42e6",
        // translatable field
        "name": "Raumschiff",
        // translatable field
        "description": "Deutsches Lorem ipsum dolor sit amet, consectetur adipiscing elit. In erat mauris, faucibus quis pharetra sit amet.",
        "image": "//a.storyblok.com/f/44203/6016x4016/995fde1190/spaceship.jpg",
        "price": "1700000000",
        "component": "product"
      },
      "slug": "spaceship",
      "full_slug": "de/products/spaceship"
      ...
    },
    ...
    {
      "name": "Shoe",
      "lang": "de",
      "created_at": "2018-12-10T17:49:40.741Z",
      "published_at": "2018-12-10T18:27:01.870Z",
      "id": 461932,
      "uuid": "9176c97c-2602-4878-80f0-ea89c9eb26b7",
      "content": {
        "_uid": "89dbca77-6df2-4c42-bcd5-a2d81277fe4b",
        // translatable field
        "name": "Schuh",
        // translatable field
        "description": "Deutsches Lorem ipsum dolor sit amet, consectetur adipiscing elit. In erat mauris, faucibus quis pharetra sit amet.",
        "image": "//a.storyblok.com/f/44203/2880x1920/3af2f49951/shoe.jpg",
        "price": "10",
        "component": "product"
      },
      "slug": "shoe",
      "full_slug": "de/products/shoe",
      ...
    }
  ]
}
```
