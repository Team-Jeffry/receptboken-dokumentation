# API

## POST

### Find recipe(s)
<br>

**/v1/recipe/find**
<br>
***RequestBody (All fields optional)***
```
{
    category: String,
    name: String,
    time: int
}
```
***returns HttpStatus 200 and ResponseBody with list of matches***
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

***RequestBody***
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
***returns HttpStatus 200 & ResponseBody***
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

***RequestBody***
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
***returns HttpStatus 200 & ResponseBody***
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