A company wants to extract its contacts from Hubspot and save them in a Google Sheet.

This exercise focuses only on the first part.

### 1- Go to 🔗 this documentation (endpoint tab) and study the endpoint /crm/v3/objects/contacts.
What are the scheme, the host, the path and the three main possible query parameters?

+ url : https://api.hubapi.com/crm/v3/objects/contacts
+ scheme = https
+ the host = api.hubapi.com
+ the path = crm/v3/objects/contacts
+ q1 = limit
+ q2 = after
+ q3 = properties

2- Access all contacts with the provided token. How does authentication work here? Is it a query parameter?
+ In header tab : use of : authorization Bearer *token*
+ No it's a header parameter


3- Use Insomnia to get the first 10 contacts from the CRM using a GET request.
+  https://api.hubapi.com/crm/v3/objects/contacts?limit=10


4- How many properties are returned per contact? 
+ 11

Can you limit the properties in a query? 
+ it's possible to specify the requierd properties

What are some of the properties that are always returned? 
+ id
+ createddate
+ lastmodifiedate
  
Why are they returned?
+ to give the most acurate information regarding the contact and be sure it's a unique contact or the good one

Try by returning email and firstname as the only properties.
+ https://api.hubapi.com/crm/v3/objects/contacts?limit=10&properties=fisrtname,email

5- Let’s say that now we only want the email and first name properties for the first 20 contacts, what do you change in Insomnia? 
+ limit and properties values

How can you get the next 20 contacts? Look carefully at the documentation.
+ by addin the after property and setting it to 120 (last contact id of thes previous request)
+ https://api.hubapi.com/crm/v3/objects/contacts?limit=20&properties=lastname,email&after=120

6- We would like to insert the results in a Google Sheet, what could we do?
Your task is to brainstorm with your buddy, you do not need to implement anything.
+ By using a JSON to CSV online tool : https://www.convertcsv.com/json-to-csv.htm


7- From Insomnia, download the Python code that produces the same API request.

```
import requests

url = "https://api.hubapi.com/crm/v3/objects/contacts"

querystring = {"limit":"20","after":"120","properties":"lastname"}

payload = ""
headers = {
    "User-Agent": "insomnia/9.2.0",
    "authorization": "Bearer ***"
}

response = requests.request("GET", url, data=payload, headers=headers, params=querystring)

print(response.text)
data = res.read()

print(data.decode("utf-8"))
```
