
# How Data Scientists Can Use Generative AI
Data scientists can go beyond just analyzing data—they can design powerful AI solutions that solve real-world problems. They can create AI tools like:

AI assistants (like chatbots that help customers)
Supply chain optimizers (AI that improves delivery efficiency)
Personalized recommendation systems (AI that suggests products, movies, or content based on user preferences)
Amazon Bedrock – A Powerful AI Tool for Data Scientists
Amazon Bedrock provides AI models that can help data scientists with natural language processing (NLP) tasks. Here’s how it can be used:

1. Text Summarization
Imagine you have a huge research paper but don’t have time to read it all. Amazon Bedrock can summarize it in a few sentences, helping you quickly understand the key points.
✅ Use case: Helps in summarizing reports, cleaning data, and analyzing text efficiently.

2. Text Generation
AI models can generate text, which is useful for:

Creating extra training data for machine learning models.
Generating code snippets (e.g., writing Python scripts automatically).
Explaining how a model works in simpler terms.
✅ Example: If you're training an AI to recognize customer complaints, but you don’t have enough complaint samples, AI can generate more examples to improve training.

✅ Tools used: Amazon Bedrock, LangChain, Retrieval-Augmented Generation (RAG) (which helps AI remember important details).

3. Question Answering Systems
These systems can answer questions automatically by searching through documents and databases.
✅ Example: Instead of reading a 100-page company manual, you can ask, "What is the refund policy?", and the AI will find the answer for you.

✅ Use case: Saves time for customer support, researchers, and developers.

✅ Tech used: RAG AI assistants can interact with knowledge bases and provide relevant answers instantly.

4. AI Agents (Amazon Bedrock Agents)
Amazon Bedrock Agents act like smart assistants that understand natural language and take action.

✅ Example: Imagine you're ordering a flight ticket. Instead of filling out multiple forms, you just say:
"Book me a round-trip flight from New York to Los Angeles next weekend."
The AI agent will:

Understand your request.
Look up flight options via APIs.
Confirm details and book your ticket.
✅ Use case: Automates complex tasks like customer service, booking systems, or data lookups.

✅ Features:

Handles security, permissions, and monitoring automatically.
Integrates with Amazon Bedrock Guardrails to prevent incorrect or unwanted responses.

# TOdo
Note: For users with screen readers, use table mode to read the following tables.


Module 2: Foundation Models

Module 3: Application Components

Module 4: Using LangChain

Lab / Demo: Explore Generative AI Use Cases with LangChain and Amazon Bedrock

Module 5: Using Knowledge Bases

Lab / Demo: Build and Evaluate RAG Applications using Amazon Bedrock Knowledge Bases

Module 6: Using Agents

Lab / Demo: Explore Amazon Bedrock Agents Integrated with Amazon Bedrock Knowledge Bases and Guardrails


# module 2
Different AI Models and Their Uses
1. Amazon Titan (by Amazon)
What it is: A family of powerful, general-purpose AI models trained on large datasets.
Use case: Can be used for a variety of AI tasks like text generation, chatbots, and automation.
2. AI2I Labs – Jurassic-2 & Jumba
What it is: Multilingual AI models for text generation.
Languages: Spanish, French, German, Portuguese, Italian, Dutch.
Use case: Creating chatbots, translations, and AI assistants that understand multiple languages.
3. Anthropic – Claude 3
What it is: A powerful AI model designed for intelligent, fast, and cost-effective responses.
Use case: Customer support, business automation, and decision-making AI.
4. Cohere – Command & Embed
Command Model: Generates text for business applications (e.g., reports, emails, chatbots).
Embed Model: Used for search, clustering, and classification in 100+ languages.
Use case: AI for business intelligence, organizing data, and multilingual applications.
5. Meta – Llama
What it is: AI models for chatbots, virtual assistants, and translations.
Use case: Can be used in social media, customer service, and global communication.
6. Mistral AI – Mistral/Mixtral
What it is: Models designed for:
✅ Text generation
✅ Code generation
✅ Retrieval-Augmented Generation (RAG)
✅ AI agents
Use case: Can be used for coding assistance, AI-powered research, and chatbot applications.
7. Stability AI – Stable Diffusion
What it is: A text-to-image model that generates high-quality images, art, and designs.
Now available: Stable Diffusion XL (SDXL) 1.0 for even better quality.
Use case: Used in graphic design, marketing, logo creation, and digital art.

How to Control AI's Randomness & Diversity
AI models generate text based on probability, but we can control how random or focused their responses are using these settings:

1. Temperature
What it does: Controls how "creative" the AI is.
Low temperature (e.g., 0.2): More predictable, logical responses.
High temperature (e.g., 0.9): More random and creative responses.
✅ Example:
Low temp (0.2):
🗣️ "What is the capital of France?"
🤖 "The capital of France is Paris."

High temp (0.9):
🗣️ "What is the capital of France?"
🤖 "Paris, but historically, Versailles was also important!"

2. Top-K Sampling
What it does: Limits AI to choosing from the K most probable words.
Low K (e.g., 10): AI picks from the top 10 most likely words → more controlled responses.
High K (e.g., 50+): AI picks from a wider range of words → more diverse responses.
✅ Example:
🗣️ "AI can be used for..."

K = 10: "AI can be used for automation, healthcare, finance, and education."
K = 50: "AI can be used for art, poetry, simulations, gaming, research, virtual worlds, and more!"
Why This Matters?
For precise, fact-based tasks (e.g., customer service, technical queries) → Use low temperature & low K.
For creativity & brainstorming (e.g., marketing, storytelling) → Use high temperature & high K.

How to Control AI's Response Length
AI models can generate short or long responses, and you can adjust their length using these settings:

1. Response Length
What it does: Sets a limit on the number of words or tokens in the response.
Short length (e.g., 20 tokens): Concise and to the point.
Long length (e.g., 200+ tokens): Detailed and elaborate responses.
✅ Example:
🗣️ "Explain climate change."

Short response (20 tokens): "Climate change refers to long-term shifts in temperature and weather patterns."
Long response (200 tokens): "Climate change refers to long-term shifts in temperature and weather patterns due to human activities like burning fossil fuels, deforestation, and industrial emissions. It leads to rising global temperatures, extreme weather events, and disruptions to ecosystems."
2. Length Penalty
What it does: Encourages shorter or longer responses by penalizing or rewarding length.
Higher penalty: AI avoids long-winded answers (useful for summaries).
Lower penalty: AI gives detailed responses (useful for explanations).
✅ Example:
If you set a high length penalty, AI will give shorter, more direct answers instead of rambling.

3. Stop Sequences
What it does: Defines specific words or phrases where the AI should stop generating text.
Useful for: Ensuring AI doesn't generate unnecessary or off-topic content.
✅ Example:
If you set the stop sequence as "End of response.", the AI will stop as soon as it generates that phrase.

🗣️ "Give me a summary of AI."
🤖 "AI stands for Artificial Intelligence. It allows machines to learn and make decisions. End of response."

Why This Matters?
For short summaries or quick answers: Use low response length + high length penalty.
For detailed explanations: Use high response length + low length penalty.
For structured responses: Use stop sequences to maintain clarity.



# 🔹 AI21 Jurassic-2 (Mid & Ultra) – Detailed Explanation with Examples
The Jurassic-2 models from AI21 Labs are powerful text generation AI models. They generate human-like text and can be fine-tuned using various parameters to control response length, randomness, and repetition.

📍 Common Parameters in Jurassic-2
✅ 1. Max Completion Length (maxTokens) → Controls Response Length
What it does: Limits the number of words or tokens the AI can generate.
Why it matters: Prevents AI from generating too much or too little text.
Example:
🔹 Max Tokens = 10
📝 Prompt: "Tell me about AI."
💬 Response: "AI is a technology that enables machines to..."

🔹 Max Tokens = 50
📝 Prompt: "Tell me about AI."
💬 Response: "AI, or Artificial Intelligence, is a branch of computer science that enables machines to simulate human intelligence. It includes machine learning, natural language processing, and more."

✅ 2. Stop Sequences (stopSequences) → Stops AI at a Specific Word or Phrase
What it does: Tells AI to stop generating text after a certain word, phrase, or punctuation.
Why it matters: Useful when you want AI to stop at a specific point in its response.
Example:
🔹 Stop Sequence = "End of response."
📝 Prompt: "Tell me about AI. Stop at 'End of response.'"
💬 Response: "AI is a field of computer science that focuses on creating intelligent machines. End of response."

🔹 Stop Sequence = "Thank you."
📝 Prompt: "Explain machine learning. Stop at 'Thank you.'"
💬 Response: "Machine learning is a subset of AI that allows computers to learn from data without explicit programming. It is used in recommendation systems, fraud detection, and more. Thank you."

📍 Parameters to Reduce Repetitions
✅ 3. Presence Penalty (presencePenalty) → Avoids Repeating Words from the Prompt
What it does: Prevents AI from using the same words from the prompt in the response too often.
Why it matters: Helps AI generate more creative and diverse responses.
Example:
🔹 Without Presence Penalty:
📝 Prompt: "What is a dog?"
💬 Response: "A dog is a pet. A dog is an animal. A dog is a mammal."

🔹 With Presence Penalty:
📝 Prompt: "What is a dog?"
💬 Response: "A dog is a domesticated animal known for its loyalty. It belongs to the Canidae family and is a popular pet worldwide."

✅ 4. Count Penalty (countPenalty) → Prevents Overuse of Words
What it does: Lowers the chance of repeating words in a response.
Why it matters: Keeps the response concise and natural.
Example:
🔹 Without Count Penalty:
📝 Prompt: "Tell me about cats."
💬 Response: "Cats are small, furry animals. Cats like to sleep. Cats are playful pets. Cats are curious animals."

🔹 With Count Penalty:
📝 Prompt: "Tell me about cats."
💬 Response: "Cats are small, furry pets known for their independence and curiosity. They enjoy sleeping, playing, and exploring their surroundings."

✅ 5. Frequency Penalty (frequencyPenalty) → Prevents Overuse of Frequently Used Words
What it does: Reduces the chance of overusing common words.
Why it matters: Helps make AI responses more natural and varied.
Example:
🔹 Without Frequency Penalty:
📝 Prompt: "Describe a beach."
💬 Response: "A beach has sand. A beach has water. A beach is relaxing. A beach is beautiful."

🔹 With Frequency Penalty:
📝 Prompt: "Describe a beach."
💬 Response: "A beach is a scenic coastal area with golden sand and waves gently crashing onto the shore. People visit beaches to relax, swim, and enjoy the sun."

📍 Penalizing Special Tokens
These settings prevent overuse of specific characters, numbers, and words.

✅ 6. Penalizing Whitespaces (applyToWhitespaces) → Prevents Extra Spaces and New Lines
What it does: Avoids too many blank spaces or unnecessary new lines.
Example (Without Penalty):

css
Copy
Edit
AI is  
a technology   
that enables  
machines to learn.
Example (With Penalty):

css
Copy
Edit
AI is a technology that enables machines to learn.
✅ 7. Penalizing Punctuation (applyToPunctuation) → Prevents Too Many Punctuation Marks
What it does: Stops AI from overusing commas, periods, question marks, etc.
Example (Without Penalty):
📝 Prompt: "Write about AI."
💬 Response: "AI is amazing!!! AI helps people!!! AI is the future!!!"

Example (With Penalty):
📝 Prompt: "Write about AI."
💬 Response: "AI is amazing. It helps people and is the future of technology."

✅ 8. Penalizing Numbers (applyToNumbers) → Prevents Too Many Numbers in the Response
What it does: Stops AI from using too many numerical values.
Example (Without Penalty):
📝 Prompt: "Tell me about planets."
💬 Response: "There are 8 planets in the solar system. Mercury takes 88 days to orbit the sun, Venus takes 225 days, Earth takes 365 days..."

Example (With Penalty):
📝 Prompt: "Tell me about planets."
💬 Response: "The solar system has several planets, each with a unique orbit and characteristics."

✅ 9. Penalizing Stop Words (applyToStopwords) → Prevents Overuse of Common Words
What it does: Reduces repetition of words like "the," "is," "and," etc.
Why it matters: Keeps the response clear and less repetitive.
Example (Without Penalty):
📝 Prompt: "Write about technology."
💬 Response: "Technology is the best thing. Technology is the future. Technology is improving the world."

Example (With Penalty):
📝 Prompt: "Write about technology."
💬 Response: "Technology is a driving force for innovation, shaping the future with new advancements."

✅ 10. Penalizing Emojis (applyToEmojis) → Controls Emoji Usage
What it does: Allows AI to use emojis freely (default setting).
Why it matters: Useful for social media content where emojis are common.
Example:
📝 Prompt: "Write a fun message about vacations."
💬 Response: "Vacations are the best! 🌴🏖️ Relax, explore, and enjoy the sunshine! ☀️✨"



# 📍 Cohere Command – Detailed Explanation
Cohere Command is a flagship text generation model optimized for business applications such as summarization, copywriting, Q&A, and more. It prioritizes security, privacy, and responsible AI, making it ideal for enterprise use.

🔹 Standard Parameters (Similar to Other Models)
Temperature – Controls randomness of responses.
Top P – Limits token selection to a probability threshold.
Top K – Limits token selection to the top K highest-probability tokens.
Max Tokens – Sets the maximum number of tokens in the response.
Stop Sequences – Defines phrases where the response should stop.
🔹 Unique Features in Cohere Command
✅ 1. Return Likelihoods (return_likelihoods) – Shows How Likely Each Word Is
What it does: Returns a likelihood score for each token (word/character) generated.
Why it matters: Useful for understanding confidence levels in AI responses.
Options:
GENERATION → Returns likelihoods for only the generated text.
ALL → Returns likelihoods for both input and output text.
NONE → No likelihoods are returned (default setting).
Example:
🔹 Without Likelihoods (return_likelihoods: NONE)
📝 Prompt: "What is the capital of France?"
💬 Response: "The capital of France is Paris."

🔹 With Likelihoods (return_likelihoods: GENERATION)
📝 Prompt: "What is the capital of France?"
💬 Response:

vbnet
Copy
Edit
Text: "The capital of France is Paris."
Likelihood: [0.98, 0.96, 0.99, 0.97]
🔹 With Likelihoods (return_likelihoods: ALL)
📝 Prompt: "What is the capital of France?"
💬 Response:

less
Copy
Edit
Input Likelihoods: [0.99, 0.98, 0.99] 
Generated Likelihoods: [0.98, 0.96, 0.99, 0.97]
✅ 2. Stream (stream) – Returns Response in Real Time
What it does: Determines whether the AI streams the response as it is generated.
Why it matters: Improves real-time interactivity (useful for chatbots, live applications).
Options:
true → Sends the response piece by piece (like typing).
false → Returns the full response at once after generation (default).
Example:
🔹 Without Streaming (stream: false)
📝 Prompt: "Tell me a story."
💬 Response (After a Few Seconds): "Once upon a time, there was a brave knight who..."

🔹 With Streaming (stream: true)
📝 Prompt: "Tell me a story."
💬 Response (Typed in Real-Time):
📝 "Once..."
📝 "Once upon..."
📝 "Once upon a time..."

✅ 3. Number of Generations (num_generations) – Generates Multiple Outputs
What it does: Produces multiple different responses in a single request.
Why it matters: Useful for A/B testing and choosing the best response.
Default: 1
Example:
🔹 num_generations: 3 (Three different responses)
📝 Prompt: "Suggest a tagline for an eco-friendly brand."
💬 Response 1: "Go green, live clean."
💬 Response 2: "Sustainability starts with you."
💬 Response 3: "Protect nature, embrace the future."

📍 Input Configuration Example
This is how a request to Cohere Command would look in JSON format:

json
Copy
Edit
{
  "prompt": "Write a summary of AI ethics.",
  "temperature": 0.7,
  "p": 0.9,
  "k": 50,
  "max_tokens": 200,
  "stop_sequences": ["End of summary."],
  "return_likelihoods": "GENERATION",
  "stream": true,
  "num_generations": 2
}
📌 Breakdown of Configuration:
Prompt: "Write a summary of AI ethics." (The instruction to AI)
Temperature: 0.7 (Balanced creativity & accuracy)
Top P: 0.9 (Diverse but controlled token selection)
Top K: 50 (Limits selection to top 50 words)
Max Tokens: 200 (Caps response at 200 tokens)
Stop Sequences: "End of summary." (Stops at this phrase)
Return Likelihoods: "GENERATION" (Returns confidence levels of output tokens)
Stream: true (Returns response in real-time)
Num Generations: 2 (Gives two different responses)