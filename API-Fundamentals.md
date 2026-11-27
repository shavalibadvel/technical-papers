## API Fundamentals 

Software applications communicate with each other constantly to share data and trigger actions. Below is how core **API** concepts work, pairing everyday analogies with the essential technical terms you will see in real-world documentation.

---

## 1. What is an API?
Think of a waiter at a restaurant. You sit at your table (the **client**, such as your phone or web browser), and the kitchen (the **server** and **database**) prepares the food. You do not walk into the kitchen yourself. Instead, you tell the waiter what you want, the waiter takes your order to the kitchen, and brings your food back.

**An API (Application Programming Interface) is that waiter.**
* **Core Concept:** It acts as a secure middleman and contract between two software systems, exposing specific **endpoints** (URLs) so applications can share data without exposing their internal code or database.

## 2. REST and SOAP
These are the two most common architectural styles for how the waiter formats and delivers your order.
* **REST (Representational State Transfer):** Like a quick, standardized sticky note. It is lightweight, fast, **stateless** (the server does not need to remember past requests), and usually sends data in **JSON** (JavaScript Object Notation) format. Almost all modern web and mobile apps use REST.
* **SOAP (Simple Object Access Protocol):** Like a thick, formal legal contract sealed in an envelope. It relies strictly on **XML** formatting, enforces rigid security and structure rules, and is mostly used in banking, healthcare, and legacy enterprise systems.

## 3. HTTP and HTTPS
This is the network road the waiter travels on between the client and the server.
* **HTTP (Hypertext Transfer Protocol):** A standard open road. Data travels in plain text, meaning anyone intercepting the connection could read the message.
* **HTTPS (HTTP Secure):** An armored truck on that same road. It uses **TLS/SSL encryption** to scramble the data in transit, protecting sensitive information like passwords, API keys, and payment details.

## 4. Request and Response
Every API interaction follows a structured **Request–Response cycle** between the client and the server.
* **Request:** The client reaches out to a specific **endpoint** (e.g., `https://api.example.com/orders`) asking for data or an action (*“Can I please have a cheeseburger?”*).
* **Response:** The server processes the request and sends back a status code along with the requested data (*“Here is your cheeseburger”* or *“Out of stock”*).

## 5. HTTP Methods (CRUD Operations)
These verbs define the exact action the client wants the server to perform on a **resource** (commonly mapped to **CRUD**: Create, Read, Update, Delete):
* **GET (Read):** *“Show me the menu.”* Retrieves data from the server without modifying anything.
* **POST (Create):** *“Add this brand-new dish to the menu.”* Submits new data to create a new resource.
* **PUT (Full Update/Replace):** *“Replace my entire burger order with a chicken sandwich.”* Overwrites an existing resource completely.
* **PATCH (Partial Update):** *“Keep my burger, just swap pickles for extra cheese.”* Modifies only specific fields of an existing resource.
* **DELETE (Delete):** *“Cancel my order.”* Removes a specific resource from the server.

## 6. HTTP Status Codes
Instead of sending a long explanation, the server returns a standardized **3-digit status code** so the client immediately knows the outcome:
* **1xx (Informational):** It gives information **100 Continue**.
* **2xx (Success):** The request worked. Common examples: **200 OK** (data returned) , **201 Created** (new resource successfully saved) and **204 No Content **.
* **3xx (Redirection):** It is about giving directions about request response like **301 Moved Permanently** , **304 Not Modified**.
* **4xx (Client Error):** Something was wrong with the request. Common examples: **400 Bad Request** (invalid formatting), **401 Unauthorized** (missing or invalid authentication), and **404 Not Found** (the endpoint or item does not exist).
* **5xx (Server Error):** The client's request was valid, but the server failed. Common example: **500 Internal Server Error** (the backend crashed or timed out).

## 7. Headers
Headers are metadata sticky notes attached to the outside of a Request or Response envelope. They do not contain the main data, but carry crucial instructions and context:
* **Authorization:** Passes credentials like a **Bearer Token** or **API Key** (*“Here is my VIP pass”*).
* **Content-Type:** Tells the receiver what format the data is in, such as `application/json` (*“This message is written in JSON”*).

## 8. Query Parameters
Query parameters are optional key-value pairs added to the end of a URL after a `?` to **filter, sort, or paginate** results.
* **Example:** `/toys?color=red&max_price=10`
* **Core Concept:** They let you narrow down a broad collection of data without changing the core endpoint path.

## 9. Path Parameters
Path parameters are dynamic variables embedded directly inside the URL path to identify **one specific resource**.
* **Example:** `/users/42/dogs/7`
* **Core Concept:** Here, `42` and `7` act like an exact street address pointing directly to User #42 and their 7th dog, rather than searching a list.

## 10. Request Body and Response Body (Payload)
While Headers are the labels on the outside, the **Body** (or **payload**) is the actual data package carried inside—most commonly formatted as **JSON**.
* **Request Body:** The data the client sends to the server during `POST`, `PUT`, or `PATCH` requests (e.g., submitting `{"username": "alex", "theme": "dark"}` when creating an account).
* **Response Body:** The structured data the server sends back to the client (e.g., returning your new `user_id`, profile details, and account timestamps).
