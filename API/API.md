# API

## POST

### Find recipe(s)

<br>

**/v1/recipe/find**
<br>
**_RequestBody (All fields optional)_**

```
{
    category: String,
    name: String,
    time: int
}
```

**_returns HttpStatus 200 and ResponseBody with list of matches_**

```
[
	{
	    "id": int,
	    "ingredients": [
            {
                id: int,
                name: String,
                description: String
            },
            ...
        ],
        "categories": [
            {
                id: int,
                name: String,
                description: String
            },
            ...
        ],
        description: String,
        instructions: String,
        time: int,
	},
	...
]
```

<br>

### Create a recipe

**/v1/recipe/save**
<br>

**_RequestBody_**

```
    {
	    "ingredients": [
            {
                name: String,
                description: String
            },
            ...
        ],
        "categories": [
            {
                name: String,
                description: String
            },
            ...
        ],
        description: String,
        instructions: String,
        time: int,
	}
```

**_returns HttpStatus 200 & ResponseBody_**

```
    {
	    "id": int,
	    "ingredients": [
            {
                id: int,
                name: String,
                description: String
            },
            ...
        ],
        "categories": [
            {
                id: int,
                name: String,
                description: String
            },
            ...
        ],
        description: String,
        instructions: String,
        time: int,
	}
```

<br>

### Suggest a recipe

**/v1/recipe/suggest**
<br>

**_RequestBody_**

```
   {
       "ingredients": [
           {
               "name": String,
               "description": String
           }
       ]
   }
```

**_returns HttpStatus 200 & ResponseBody_**

```
[
	{
	    "id": int,
	    "ingredients": [
            {
                id: int,
                name: String,
                description: String
            },
            ...
        ],
        "categories": [
            {
                id: int,
                name: String,
                description: String
            },
            ...
        ],
        description: String,
        instructions: String,
        time: int,
	},
	...
]
```
