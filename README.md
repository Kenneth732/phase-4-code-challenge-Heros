# Hero API
This is a Rails API that provides information about superheroes and their powers. The API uses Active Model Serializers to serialize data.

# Prerequisites
Ruby 2.7.2
Rails 6.1.3
PostgreSQL 12

# Installation

1 Clone the repository:

```
git clone git@github.com:your-username/hero-api.git

```

2 Install dependencies:

```
bundle install
```

3 Create the database:

```
rails db:create
```

4 Run migrations:
```
rails db:migrate
```
5 Start the server:
```
rails server
```

# Usage
The API has the following endpoints:

# GET /heroes
Returns a list of all superheroes.

Example response:

```
[  {    "id": 1,    "name": "Spider-Man",    "real_name": "Peter Parker",    "created_at": "2023-03-23T14:15:16.000Z",    "updated_at": "2023-03-23T14:15:16.000Z",    "powers": [      {        "id": 1,        "name": "Spider-Sense",        "description": "Ability to sense danger"      },      {        "id": 2,        "name": "Web-Slinging",        "description": "Ability to shoot webs"      }    ]
  },
  {
    "id": 2,
    "name": "Iron Man",
    "real_name": "Tony Stark",
    "created_at": "2023-03-23T14:15:16.000Z",
    "updated_at": "2023-03-23T14:15:16.000Z",
    "powers": [
      {
        "id": 3,
        "name": "Flight",
        "description": "Ability to fly"
      },
      {
        "id": 4,
        "name": "Repulsor Rays",
        "description": "Ability to shoot energy beams from hands"
      }
    ]
  }
]

```

# GET /heroes/:id
Returns information about a specific superhero.

Example response

```
{
  "id": 1,
  "name": "Spider-Man",
  "real_name": "Peter Parker",
  "created_at": "2023-03-23T14:15:16.000Z",
  "updated_at": "2023-03-23T14:15:16.000Z",
  "powers": [
    {
      "id": 1,
      "name": "Spider-Sense",
      "description": "Ability to sense danger"
    },
    {
      "id": 2,
      "name": "Web-Slinging",
      "description": "Ability to shoot webs"
    }
  ]
}

```

# POST /hero_powers
Creates a new superhero power and associates it with a superhero.

Example request body

```
{
  "strength": 5,
  "power_id": 1,
  "hero_id": 1
}

```

# Example response:

```
{
  "id": 1,
  "name": "Spider-Sense",
  "description": "Ability to sense danger",
  "created_at": "2023-03-23T14:15:16.000Z",
  "updated_at": "2023-03-23T14:15:16.000
}
```