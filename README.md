# Cybersecurity Awareness Chatbot — Part 1 & Part 2

## Project Overview

This Cybersecurity Awareness Chatbot is an interactive console-based application developed in **C# using .NET Framework 4.8**. It is divided into two development phases:

- **Part 1**: A rule-based chatbot that greets users, remembers their name, responds to cybersecurity-related queries, and educates them on safe online behavior.
- **Part 2**: An advanced chatbot version that includes **machine learning sentiment detection**, **text-to-speech**, and **keyword recognition**, enhancing user interaction by detecting emotions and tailoring responses accordingly.

---

## Part 1: Basic Cybersecurity Chatbot

### Features
- Plays a voice greeting at startup using `System.Media.SoundPlayer`.
- Displays a custom ASCII Art logo.
- Greets the user, asks their name, and remembers it.
- Explains what cybersecurity is if the user has no prior knowledge.
- Presents a menu with 3 cybersecurity topics:
  - Password Safety
  - Phishing
  - Safe Browsing
- Provides lengthy explanations for each topic.
- Recognizes basic user questions like "how are you?" or "what can I ask you?"
- Simulates human-like typing delays using `Thread.Sleep()`.
- Loops until the user exits by typing `4`.

### Libraries Used

| Library | Purpose |
|--------|---------|
| `System` | Provides core functionalities like input/output and exception handling. |
| `System.Media` | Plays `.wav` sound files for greetings. |
| `System.Threading` | Simulates typing with delay effects for realism. |

---

## Part 2: Enhanced Chatbot with Sentiment Detection

### Features
- Remembers user’s interest (e.g., privacy, scams).
- Uses ML.NET to train and detect user sentiment:
  - Detects positive emotions (e.g., "I love cybersecurity")
  - Detects negative emotions (e.g., "I'm worried", "I'm confused")
- Text-to-speech responses using `System.Speech.Synthesis`.
- Rotating, dynamic responses using Dictionaries and Lists.
- Shows additional tips when keywords like "password", "privacy", or "phishing" are mentioned.
- Presents phishing tips and best practices randomly.
- Uses an ASCII art logo for a polished greeting.
- Structured using methods and reusable components.

### Additional Libraries in Part 2

| Library | Purpose |
|--------|---------|
| `Microsoft.ML` | Enables training and using a logistic regression model for sentiment classification. |
| `Microsoft.ML.Data` | Defines data structures for model input and output. |
| `System.Speech.Synthesis` | Allows the chatbot to speak aloud responses. |
| `System.Collections.Generic` | Manages lists and dictionaries for dynamic tip generation. |

---

## Example Topics & Responses

### Password Safety
- Use a mix of symbols, numbers, and upper/lowercase characters.
- Never reuse passwords across websites.
- Use password managers and two-factor authentication wherever possible.

### Phishing
- Be cautious of urgent emails or texts asking for information.
- Verify senders before clicking links.
- Avoid downloading unknown attachments.

### Safe Browsing
- Use HTTPS websites.
- Avoid public Wi-Fi for banking or sensitive transactions.
- Keep your browser and antivirus updated.

---

## How to Use

### Running the Project
1. Clone the repository or open it in Visual Studio.
2. Ensure your .NET Framework version is 4.8 or higher.
3. Part 1: Run `CybersecurityChatbot.cs`
4. Part 2: Run the enhanced chatbot with sentiment detection (`Program.cs` in Part 2).
5. Ensure `.wav` file paths are valid for voice greeting in Part 1.
6. For Part 2, confirm that `Microsoft.ML` and `System.Speech` are added as references.

### Accessing the Repository
If your project is hosted on GitHub:

```bash
git clone https://github.com/your-username/cybersecurity-chatbot.git
cd cybersecurity-chatbot
