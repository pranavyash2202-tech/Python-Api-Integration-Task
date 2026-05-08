
# 🚀 Python API Integration & JSON Handling

A Python project demonstrating API communication, JSON parsing, filtering logic, and error handling using the Requests library.

---

# 📌 Objective

Learn how Python communicates with external APIs and handles JSON data efficiently.

---

# ✅ Features

- Fetch data using Requests library
- Parse JSON responses
- Apply filtering/search logic
- Handle API errors
- Display formatted output

---

# 🛠️ Technologies Used

- Python
- Requests Library
- JSONPlaceholder API
- VS Code

---

# 🌐 API Used

```text
https://jsonplaceholder.typicode.com/users
```

---

# 📂 Project Structure

```text
python-api-integration-task/
│
├── api_task.py
├── README.md
├── screenshots/
│   ├── code.png
│   └── output.png
└── Task_3_Report.docx
```

---

# ⚙️ Installation

Install required library:

```bash
pip install requests
```

---

# ▶️ Run the Program

```bash
python api_task.py
```

---

# 💻 Python Code

```python
import requests

# API URL
url = "https://jsonplaceholder.typicode.com/users"

try:
    # Sending GET request
    response = requests.get(url)

    # Check if request successful
    response.raise_for_status()

    # Convert response into JSON
    users = response.json()

    print("===== USER DETAILS =====\n")

    # Search/filter logic
    search_city = "South Christy"

    found = False

    for user in users:
        if user["address"]["city"] == search_city:
            found = True

            print(f"Name     : {user['name']}")
            print(f"Username : {user['username']}")
            print(f"Email    : {user['email']}")
            print(f"City     : {user['address']['city']}")
            print("-" * 30)

    if not found:
        print("No users found in the searched city.")

# Error handling
except requests.exceptions.HTTPError as errh:
    print("HTTP Error:", errh)

except requests.exceptions.ConnectionError:
    print("Error Connecting to API")

except requests.exceptions.Timeout:
    print("Request Timed Out")

except requests.exceptions.RequestException as err:
    print("Something went wrong:", err)
```

---

# 📸 Output

```text
===== USER DETAILS =====

Name     : Chelsey Dietrich
Username : Kamren
Email    : Lucio_Hettinger@annie.ca
City     : South Christy
------------------------------
```

---

# 🔍 Concepts Implemented

✅ API Communication  
✅ JSON Parsing  
✅ Filtering Logic  
✅ Error Handling  

---

# 📄 Report

Detailed report available in:

```text
Task_3_Report.docx
```

---

# 👨‍💻 Author

**Pranav Ranjan**  


---

# ⭐ Project Status

✅ Completed  
✅ Internship Ready  
✅ Beginner Friendly
