# API


<br>

## POST

### Find recipe(s)
**/v1/recipe/find**
<br>
<br>
***RequestBody (All fields optional)***
```
{
    category: String,
    name: String,
    ingredients: []
}
```
***returns HttpStatus 200 and ResponseBody with list of matches***
```
[
	{
	    "id": int,
	    "employee": {
		"id": int,
		"identification": String,
		"firstName": String,
		"surname": String
	    },
	    "item": {
		"id": int,
		"type": {
			"id": int,
			"name": String
		},
		"description": String
	    },
	    "comment": String,
	    "active": boolean,
	    "dateLoaned": LocalDateTime,
	    "dateReturned": LocalDateTime,
	    "receivedBy": String,
	    "returnedBy": {
		"id": int,
		"identification": String,
		"firstName": String,
		"surname": String
	    }
	},
	...
]
```

<br>

### Create a loan
**/v1/loan**
<br>

***RequestBody***
```
{
    "comment": String,
    "identification": String,
    "firstName": String,
    "surname": String,
    "itemType": String,
    "itemDescription": String
}
```
***returns HttpStatus 200 & ResponseBody***
```
{
    "id": int,
    "employee": {
    	"id": int,
	"identification": String,
	"firstName": String,
	"surname": String
    },
    "item": {
    	"id": int,
	"type": {
		"id": int,
		"name": String
	},
	"description": String
    },
    "comment": String,
    "active": boolean,
    "dateLoaned": LocalDateTime,
    "dateReturned": LocalDateTime,
    "receivedBy": String,
    "returnedBy": {
    	"id": int,
	"identification": String,
	"firstName": String,
	"surname": String
    }
}
```

## PUT
<br>

### Return loan
**/v1/loan**
<br>

***RequestBody***
```
{
    "loanId": int,
    "recievedBy": String,
    "returnedBy": {
    	"identification": String,
	"firstName": String,
	"surname": String
    },
}
```

***returns httpStatus 200 and ResponseBody***
```
{
    "id": int,
    "employee": {
    	"id": int,
	"identification": String,
	"firstName": String,
	"surname": String
    },
    "item": {
    	"id": int,
	"type": {
		"id": int,
		"name": String
	},
	"description": String
    },
    "comment": String,
    "active": boolean,
    "dateLoaned": LocalDateTime,
    "dateReturned": LocalDateTime,
    "receivedBy": String,
    "returnedBy": {
    	"id": int,
	"identification": String,
	"firstName": String,
	"surname": String
    }
}
```

<br>

### Update loan
**/v1/loan/update/{loanId}**
<br>

***RequestBody***
```
{
	"comment": String (Comment about the loan - optional)
	"itemType": String (Type of item - optional)
	"itemDescription": String (Serialnumber/modelname - optional)
}
```
***returns httpStatus 200 & ResponseBody***
```
{
    "id": int,
    "employee": {
    	"id": int,
	"identification": String,
	"firstName": String,
	"surname": String
    },
    "item": {
    	"id": int,
	"type": {
		"id": int,
		"name": String
	},
	"description": String
    },
    "comment": String,
    "active": boolean,
    "dateLoaned": LocalDateTime,
    "dateReturned": LocalDateTime,
    "receivedBy": String,
    "returnedBy": {
    	"id": int,
	"identification": String,
	"firstName": String,
	"surname": String
    }
}
```

<br>

### Update employee
**/v1/employee/update/{employeeIdentification}**
<br>

***RequestBody***
```
{
	"identification": String,
	"firstName": String,
	"surname": String
}
```
***returns httpStatus 200 & ResponseBody***
```
{
    "employee": {
    	"id": int,
	"identification": String,
	"firstName": String,
	"surname": String
    }
}
```