
---

## **KYR-HR-ASSIST Agentic AI System**

---

KYR-HR-ASSIST is an Agentic AI system designed to help HR teams automate routine workflows.
This implementation demonstrates automation of the **employee onboarding process**, streamlining repetitive HR tasks that typically require manual intervention.

In terms of technical architecture, for the MCP client we use **Claude Desktop**, and this repository represents the **MCP server** with all the necessary tools that will be accessed by the MCP client.

---

### 🛠️ **Setup Instructions**

To set up and run **KYR-HR-ASSIST**, follow these steps carefully:

#### 1. Configure `claude_desktop_config.json`

Add the following configuration to your **Claude Desktop** configuration file:

```json
{
  "mcpServers": {
    "kyr-hr-assist": {
      "command": "C:\\Users\\Your_Path_name\\.local\\bin\\uv",
      "args": [
        "--directory",
        "C:\\Code\\kyr-hr-assist",
        "run",
        "server.py"
      ],
      "env": {
        "KYR_EMAIL": "your_email@example.com",
        "KYR_EMAIL_PWD": "your_app_password"
      }
    }
  }
}
```

* Replace `your_email@example.com` with your **actual email ID**.
* Replace `your_app_password` with your **app-specific password** (for Gmail or other providers).
* Run the following commands to initialize the MCP environment:

```bash
uv init
uv add mcp[cli]
```

---

### 🚀 **Usage**

* Open **Claude Desktop**, click the `+` icon, and select **Add from kyr-hr-assist**.
* Fill in the required details for the new employee — the system will automatically generate onboarding workflows.

<img src="resources\\image.jpg" alt="Claude desktop prompt with fields" style="width:auto;height:300px;padding-left:30px">

Alternatively, you can craft a custom prompt and let the **KYR-HR-ASSIST agent** take full control of the process.

---

### 📘 **Project Structure**

```
kyr-hr-assist/
│
├── HRMS/
│   ├── employee_manager.py
│   ├── seeding_data.py
│   ├── ...
│
├── .env.example
├── requirements.txt
├── server.py
├── README.md
└── resources/
    └── image.jpg
```

---

### ⚖️ **License and Credits**

All rights reserved © **Mahima Kota**.
This project is for educational and demonstration purposes only.

