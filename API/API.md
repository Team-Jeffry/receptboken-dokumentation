# API

## POST

### Get recipe(s)

<br>

**/v1/recipe/get**
<br>
**_RequestBody (All fields optional)_**

```
{
    recipeName: String,
    categoryNames: [
    	String
    ],
    time: Int
}
```

**_returns HttpStatus 200 and ResponseBody with list of matches_**

```
[
      {
      	    "id": {
	        "timestamp": Int,
            	"date": String
	    },
	    "name": String,
	    "description": String,
	    "instruction": String,
	    "time": int,
	    "ingredients": [
            	{
	      	    "id": {
		        "timestamp": Int,
	            	"date": String
		    },
                    name: String,
                    description: String
            	},
     	    ],
            "categories": [
            	{
	      	    "id": {
		        "timestamp": Int,
	            	"date": String
		    },
                    name: String,
                    description: String
            	},
            ]
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

**_returns HttpStatus 200 & ResponseBody_**

```
{
	"id": {
		"timestamp": Int,
 		"date": String
    	},
	"name": String,
	"description": String,
	"instruction": String,
	"time": Int,
	"ingredients": [
            {
		"id": {
			"timestamp": Int,
			"date": String
		},
                name: String,
                description: String
            },
     	],
        "categories": [
            {
		"id": {
			"timestamp": Int,
			"date": String
		},
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

**_RequestBody_**

```
[
    {
        "name": String
    },
    ...
]
```

**_returns HttpStatus 200 & ResponseBody_**

```
[
      {
      	    "id": {
	        "timestamp": Int,
            	"date": String
	    },
	    "name": String,
	    "description": String,
	    "instruction": String,
	    "time": int,
	    "ingredients": [
            	{
	      	    "id": {
		        "timestamp": Int,
	            	"date": String
		    },
                    name: String,
                    description: String
            	},
     	    ],
            "categories": [
            	{
	      	    "id": {
		        "timestamp": Int,
	            	"date": String
		    },
                    name: String,
                    description: String
            	},
            ]
     },
     ...
]
```
