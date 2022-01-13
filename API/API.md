# API

## POST

### Find recipe(s)
<br>

**/v1/recipe/get**
<br>
***RequestBody (All fields optional)***
```
{
    recipeName: String,
    categoryName: String,
    time: int
}
```
***returns HttpStatus 200 and ResponseBody with list of matches***
```
[
      {
	    "id": int,
	    "name": String,
	    "description": String,
	    "instruction": String,
	    "time": int,
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
        ]
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
    "name": String,
    "ingredients": [
        {
            "name": String,
            "description": String
        }
    ],
    "categories": [
        {
            "name": String,
            "description": String
        }
    ],
    "description": String,
    "instruction": String,
    "time": int
}
```
***returns HttpStatus 200 & ResponseBody***
```
    {
	    "id": int,
	    "name": String,
	    "description": String,
	    "instruction": String,
	    "time": int,
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
        ]
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
	    "name": String,
	    "description": String,
	    "instruction": String,
	    "time": int,
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
        ]
     },
  ...
]
```
