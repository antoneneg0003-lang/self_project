# 🧱 What Is an API? (Explained From Absolute Zero, Very Detailed)

## 0️⃣ The Core Problem (Why API Exists)

You have 2 separate things:

- **Frontend** (website/app) → runs on user's device (browser/mobile)
- **Backend** (server) → runs on your machine/cloud and can access model + database

These two cannot magically share memory or call each other's functions directly.

So we need a **standard communication method**.

That standard method is an **API**.

---

## 1️⃣ API = A Door + Rules

Think of your backend server as a building.

- Your ML model is inside the building.
- Users (frontend) are outside.

An **API** is like a **door** with rules:

- Where is the door? (URL / route)
- What can you send through the door? (input format)
- What will you get back? (output format)
- What actions are allowed? (methods like GET/POST)
- What happens if input is invalid? (error response)

So:

**API = a defined way to request something from a server and receive a response.**

---

## 2️⃣ Who Uses an API?

APIs are made for **programs**, not humans.

Examples of "programs" that call APIs:
- Frontend website
- Mobile app
- Another backend service
- A Python script
- Postman (testing tool)

So:

Frontend does not talk to your ML model directly.  
Frontend talks to the **API**, and the API talks to the ML model.

---

## 3️⃣ What Is an Endpoint?

An API is not one single thing.

It usually has multiple "doors".

Each door is called an **endpoint**.

Example endpoints for an ML service:

- `POST /predict` → get prediction
- `GET /health` → check if server is alive
- `GET /version` → see which model version is running

Each endpoint is:
- A specific URL path (like `/predict`)
- With a specific method (GET/POST/etc.)

---

## 4️⃣ What Are GET and POST?

These are HTTP methods (types of requests).

### ✅ GET = "Give me data"
- Used when you want to **fetch** something
- Usually no big input body

Example:
- `GET /health`

### ✅ POST = "Here is input, do some work"
- Used when you want to **send input**
- Usually has a JSON body

For ML prediction:
You must send input text/features.
So prediction is usually `POST /predict`.

---

## 5️⃣ What Is JSON? (Why It Is Used)

When frontend sends input to backend, they need a shared language.

JSON is that common data format.

Example JSON:

{
  "text": "Free money now!!!"
}

JSON is just a structured way to send data:
- strings
- numbers
- lists
- objects

---

## 6️⃣ What Exactly Happens in a Prediction API Call?

Let’s walk through it step-by-step.

### Step A — Frontend prepares the data
User types:

Free money now!!!

Frontend converts it into JSON:

{
  "text": "Free money now!!!"
}

### Step B — Frontend sends request to backend API
Frontend sends:

- Method: POST
- Endpoint: /predict
- Body: JSON (contains the input)

So it sends:

POST /predict  
Body:
{
  "text": "Free money now!!!"
}

### Step C — Backend receives the request
Backend reads the JSON.

It extracts:

text = "Free money now!!!"

### Step D — Backend calls the ML model internally
Backend passes input into the ML pipeline:

- Preprocess the text
- Convert to features (vectorization / tokenizer)
- Run the model
- Get prediction score/label

### Step E — Backend creates response JSON
Backend outputs:

{
  "prediction": "spam"
}

### Step F — Frontend receives response and shows it
Frontend reads response JSON.

Then it displays on UI:

Prediction: spam

---

## 7️⃣ Why We Say “ML Engineer Builds the API”

Because the ML Engineer must create the server code that:

- Defines /predict
- Loads the trained model
- Accepts JSON input safely
- Validates input
- Runs prediction
- Returns JSON output
- Handles errors

Without API, the model is useless outside your laptop.

---

## 8️⃣ API Contract (Very Important Concept)

An API is a **contract** between frontend and backend.

It answers:

### Input contract
- What keys are required?
- What data type?
- What shape?

Example:
- Must send "text" as string

### Output contract
- What response keys exist?
- What types?
- What errors look like?

Example:
- returns "prediction" as string

If frontend breaks the contract → backend returns error.

---

## 9️⃣ Error Responses (What Happens If Input Is Wrong)

Example: Frontend sends:

{
  "message": 123
}

Backend expected "text" but got "message".

Backend returns error:

{
  "error": "Missing field: text"
}

This is part of API design too.

ML engineers must handle this cleanly.

---

## 🔟 Real Minimal API Example (Conceptual)

API endpoint /predict:

Input:
{
  "text": "Free money now!!!"
}

Output:
{
  "prediction": "spam",
  "confidence": 0.98
}

(Confidence is optional but often useful.)

---

## ✅ Final One-Line Understanding

API is the bridge that lets any program send input to your ML model (through backend) and receive the prediction back in a standard format (usually JSON).
