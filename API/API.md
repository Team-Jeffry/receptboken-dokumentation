# API

## POST

### Get recipe(s)
<br>

**/v1/recipe/get**
<br>
***RequestBody (All fields optional)***
```
{
    recipeName: String,
    categoryNames: [
    	String
    ],
    time: Int
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
     	    ],
            "categories": [
            	{
                    id: Int,
                    name: String,
                    description: String
            	},
            ]
     },
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
    "description": String,
    "instruction": String,
    "time": Int,
    "ingredients": [
        {
            "name": String,
            "description": String
        },
    ],
    "categoryNames": [
        String
    ]
}
```
***returns HttpStatus 200 & ResponseBody***
```
{
	"id": Int,
	"name": String,
	"description": String,
	"instruction": String,
	"time": Int,
	"ingredients": [
            {
                id: Int,
                name: String,
                description: String
            }, 
     	],
        "categories": [
            {
                id: Int,
                name: String,
                description: String
            },
        ]
 }
```

<br>

### Suggest a recipe
**/v1/recipe/suggest**
<br>

***RequestBody***
```
[
    {
        "name": String
    },
    ...
]
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
     	    ],
            "categories": [
            	{
                    id: Int,
                    name: String,
                    description: String
            	},
            ]
     },
]
```
