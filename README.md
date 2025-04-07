<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Zithara AI Customer Support</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
    }
    header {
      background-color: #004080;
      color: white;
      padding: 2rem;
      text-align: center;
    }
    main {
      max-width: 1000px;
      margin: 2rem auto;
      padding: 1rem;
      background: white;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .section {
      margin-bottom: 2rem;
    }
    .chatbox {
      border: 1px solid #ccc;
      border-radius: 5px;
      height: 200px;
      padding: 1rem;
      overflow-y: auto;
      margin-bottom: 1rem;
    }
    .input-row {
      display: flex;
      gap: 1rem;
    }
    .input-row input {
      flex: 1;
      padding: 0.5rem;
    }
    .faq ul {
      padding-left: 20px;
    }
    form input, form textarea {
      width: 100%;
      margin-bottom: 1rem;
      padding: 0.5rem;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    form button {
      padding: 0.7rem 1.5rem;
      background-color: #004080;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <h1>Zithara AI Customer Support</h1>
    <p>Your 24/7 smart assistant</p>
  </header>  <main>
    <div class="section">
      <h2>Chat with Zithara AI</h2>
      <div class="chatbox" id="chatbox">
        <p><em>Welcome! How can I assist you today?</em></p>
      </div>
      <div class="input-row">
        <input type="text" id="userInput" placeholder="Type your message...">
        <button onclick="sendMessage()">Send</button>
      </div>
    </div><div class="section faq">
  <h2>Frequently Asked Questions</h2>
  <ul>
    <li>How do I track my order?</li>
    <li>What is Zithara's return policy?</li>
    <li>How can I speak to a human support agent?</li>
  </ul>
</div>

<div class="section">
  <h2>Contact Human Support</h2>
  <form onsubmit="submitForm(event)">
    <input type="text" placeholder="Your Name" required />
    <input type="email" placeholder="Your Email" required />
    <textarea placeholder="Your message..." rows="4" required></textarea>
    <button type="submit">Send Message</button>
  </form>
</div>

  </main>  <script>
    function sendMessage() {
      const input = document.getElementById("userInput");
      const chatbox = document.getElementById("chatbox");
      if (input.value.trim() === "") return;

      const userMessage = document.createElement("p");
      userMessage.innerHTML = `<strong>You:</strong> ${input.value}`;
      chatbox.appendChild(userMessage);

      const aiMessage = document.createElement("p");
      aiMessage.innerHTML = `<strong>Zithara AI:</strong> Thanks for your message. We’ll get back to you shortly.`;
      chatbox.appendChild(aiMessage);

      chatbox.scrollTop = chatbox.scrollHeight;
      input.value = "";
    }

    function submitForm(event) {
      event.preventDefault();
      alert("Message sent to human support. We'll get back to you soon!");
    }
  </script></body>
</html>

<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI Customer Support Bot</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f4f4f4; }
    .chatbox { width: 400px; max-height: 600px; margin: 50px auto; background: #fff; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); overflow: hidden; display: flex; flex-direction: column; }
    .messages { flex: 1; padding: 15px; overflow-y: auto; }
    .user, .bot { margin: 10px 0; padding: 10px; border-radius: 10px; }
    .user { background: #d1e7dd; align-self: flex-end; }
    .bot { background: #f8d7da; align-self: flex-start; }
    .input-box { display: flex; border-top: 1px solid #ccc; }
    input[type="text"] { flex: 1; padding: 10px; border: none; border-radius: 0 0 0 10px; }
    button { padding: 10px; border: none; background: #0d6efd; color: white; cursor: pointer; border-radius: 0 0 10px 0; }
  </style>
</head>
<body>
  <div class="chatbox">
    <div class="messages" id="messages"></div>
    <div class="input-box">
      <input type="text" id="userInput" placeholder="Ask me anything...">
      <button onclick="sendMessage()">Send</button>
    </div>
  </div>  <script>
    function sendMessage() {
      const input = document.getElementById('userInput');
      const message = input.value.trim();
      if (message === '') return;

      addMessage('user', message);
      input.value = '';

      setTimeout(() => {
        const response = getBotResponse(message);
        addMessage('bot', response);
      }, 500);
    }

    function addMessage(sender, text) {
      const msgDiv = document.createElement('div');
      msgDiv.classList.add(sender);
      msgDiv.textContent = text;
      document.getElementById('messages').appendChild(msgDiv);
      document.getElementById('messages').scrollTop = document.getElementById('messages').scrollHeight;
    }

    function getBotResponse(input) {
      const lower = input.toLowerCase();

      if (lower.includes("hello") || lower.includes("hi")) {
        return "Hello! How can I assist you today?";
      } else if (lower.includes("price") || lower.includes("cost") || lower.includes("plan")) {
        return "We offer flexible pricing plans based on your needs. Visit our pricing page or tell me what you're looking for.";
      } else if (lower.includes("product") || lower.includes("feature")) {
        return "Our product helps streamline customer service with AI-driven solutions. Want to know about specific features?";
      } else if (lower.includes("support") || lower.includes("help")) {
        return "Our support team is available 24/7. You can reach us at support@example.com or ask me anything here!";
      } else if (lower.includes("refund") || lower.includes("return")) {
        return "We offer a 30-day refund policy. If you're not satisfied, contact support@example.com for help.";
      } else if (lower.includes("hours") || lower.includes("time")) {
        return "Our team is available Monday to Friday, 9 AM to 6 PM IST.";
      } else if (lower.includes("order") || lower.includes("status")) {
        return "Please provide your order ID and I’ll check the status for you.";
      } else {
        return "I'm not sure about that. Can you rephrase your question or provide more details?";
      }
    }
  </script></body>
</html>
