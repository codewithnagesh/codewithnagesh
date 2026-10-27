

---

# 👋 Hi, I’m Nagesh

![Laravel](https://img.shields.io/badge/Laravel-12-red?style=for-the-badge\&logo=laravel) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![Claude](https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=claude&logoColor=white) ![PHP](https://img.shields.io/badge/PHP-8+-blue?style=for-the-badge\&logo=php) ![API Security](https://img.shields.io/badge/API-Security-green?style=for-the-badge) ![Queue Jobs](https://img.shields.io/badge/Queue-Jobs-yellow?style=for-the-badge) ![Clean Code](https://img.shields.io/badge/Clean-Code-purple?style=for-the-badge)

I’m a **Laravel 12** and **PHP 8+ specialist** with **8+ years** of experience building **clean, scalable, secure, and maintainable applications, with a growing focus on Python development and AI-powered solutions.**.

Over time, I’ve noticed **small but critical details most developers miss** — things that can cause **performance issues**, **security gaps**, or make **testing harder**.

**𝗜 𝗳𝗼𝗰𝘂𝘀 𝗼𝗻 𝘄𝗵𝗮𝘁 𝗺𝗮𝗻𝘆 𝗱𝗲𝘃𝗲𝗹𝗼𝗽𝗲𝗿𝘀 𝗼𝘃𝗲𝗿𝗹𝗼𝗼𝗸:** writing modular code with **Repository / Service / Facade patterns**, preventing **N+1 query issues**, handling **background jobs ⏱️**, and enforcing **API & service-level authentication & authorization 🔐**.

I structure applications using **layered architecture**:
**Request → Controller → Action → Service → Repository → Resource**
This ensures **readability**, **testability**, and long-term **maintainability**, while optimizing ORM queries, building robust APIs, and ensuring smooth integrations.

---

## ⚡ Key Skills

* **Laravel 12 / PHP 8+** expert 🏆
* **Python Development** Python fundamentals, scripting, automation, backend integrations 🏆
* **AI Engineering** LLM integration, AI-powered APIs, prompt engineering 🏆
* **Clean Architecture & Design Patterns:** Repository, Service, Facade 🧩
* **API & Service Level Authentication/Authorization** 🔐
* **Queue Jobs & Background Processing** ⏱️
* **ORM Optimization / N+1 Query Prevention** 🔍
* **Layered Application Structure for Maintainability** 🏗️
* **API Documentation & Integration** 📄

---

## 💡 Real-World Examples

### 1️⃣ Calling LLM to summaries the video for RAG answers 🧩

```python
def gemini_chat_model(self):
        """Builds Google Gemini chat client.
        
        Temperature is set to 0 for deterministic, factual summaries and RAG answers.
        """
        return ChatGoogleGenerativeAI(
            model=self.__chat_model,
            temperature=0,
            max_output_tokens=None,
            timeout=None,
            max_retries=2,
        )
```

**Benefit:** Simplifies code, enforces type safety, and makes dependency management cleaner — improving maintainability and reducing coupling.

---

### 2️⃣ Prompt Engineering in an AI-Powered MCP Assistant 📦

```python
async def ask_question(self, state: MainState):
        """Invokes the AI agent with database tools to generate a verified answer."""
        messages = tool_calls = []
        messages.append(
            SystemMessage(
                content="""You are an MCP database assistant. Answer database queries through MCP tools.

                    Common Tables & Key Columns:
                        - `employees`: id, code, first_name, last_name, email, role, status
                        - `users`: id, full_name, email, is_active, is_verified
                        - For other tables, discover them using `get_table_names` and `get_fields`.

                    Query & Token Optimization Rules:
                        - Casual messages (hi, hello, etc.) → respond naturally without database tools.
                        - When querying wide tables (especially `employees`), ALWAYS specify only the relevant summary 
                        - For general listing requests, fetch a single page (limit=10 to 15)
                        - Never assume or invent tables, fields, records, or values.
                        - Only use tables and fields confirmed by tool results.
                        - Respond concisely in clean Markdown with relevant emojis.
                """
            )
        )
```

**Benefit:** Keeps business and database logic separate, making the application modular and easier to maintain or switch between data sources.

---

### 3️⃣ Authentication & Authorization at API and Data Levels 🔐

```php
// Sanctum API authentication
Route::middleware('auth:sanctum')->get('/profile', function (Request $request) {
    return $request->user();
});

// Policy-based authorization
if ($user->can('update', $post)) {
    $post->update(['title' => 'Updated Title']);
}
```

**Benefit:** Strengthens security at both API and ORM levels, ensuring proper access control across all layers.

---

### 4️⃣ Layered Architecture for Maintainability 🏗️

**Structure:** Request → Controller → Action → Service → Repository → Resource

**Benefit:** Enhances readability, testability, and scalability by organizing business logic clearly and reducing tight coupling.

---

## 🚀 What Others Miss — And The Advantage ⚡

Most developers skip these finer details in the rush to deliver features.
But they’re what make the real difference:

* Fewer bugs ✅
* Faster scaling ⚡
* Easier onboarding for new developers 👨‍💻
* Smoother CI/CD deployments 📦

It’s the difference between code that just **works** and code that **lasts**.

---

## 🔗 Connect with me

* [Upwork Profile] [https://www.upwork.com/freelancers/~014aa803c2d342716f?viewMode=1](url)
  

---

