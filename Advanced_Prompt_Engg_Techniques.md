# 🧠 Advanced Prompt Engineering Techniques — Hands-On Lab

> **Self-paced lab** | No coding required |
> 
> Practice directly in [ChatGPT](https://chat.openai.com) · [Claude](https://claude.ai) · [Gemini](https://gemini.google.com)

---

## 📖 How to Use This Lab Guide

This lab is self-paced. Each module has a short concept explanation followed by hands-on exercises you perform directly in the chatbot interfaces. You will compare how different AI assistants respond to the same prompts and learn what makes a prompt powerful or weak.

| Icon / Box | What it means |
|---|---|
| 🟩 **Try It box** | A specific prompt for you to copy and test in a chatbot right now |
| 🟧 **Reflection box** | Questions to think about and discuss after each activity |
| 🟦 **Info box** | Key definitions, tips, or important notes |
| **Bold text** | A term or concept being introduced for the first time |

---

## Table of Contents

- [Module 1: Advanced Patterns in Prompt Engineering](#module-1-advanced-patterns-in-prompt-engineering)
- [Module 2: Semantic Prompting and Contextual Understanding](#module-2-semantic-prompting-and-contextual-understanding)
- [Module 3: Multimodal Prompts](#module-3-multimodal-prompts)
- [Module 4: Iterative Prompt Refinement Techniques](#module-4-iterative-prompt-refinement-techniques)
- [Lab Summary & Cheat Sheet](#lab-summary--quick-reference-cheat-sheet)
- [Glossary](#glossary-of-key-terms)

---

## Module 1: Advanced Patterns in Prompt Engineering

In this module, you will move beyond simple one-line questions and learn structured prompt patterns that give you significantly more control over the AI's response style, role, and reasoning process.

### 1.1 What Is a Prompt Pattern?

A **prompt pattern** is a reusable template or structure you apply to shape how an AI responds. Think of it like a recipe — the ingredients change, but the method stays the same. Mastering a handful of patterns lets you get consistent, high-quality results across many different tasks.

#### The Six Most Powerful Prompt Patterns

| Pattern Name | What it does and when to use it |
|---|---|
| **Persona Pattern** | Tells the AI to adopt a specific role or expert identity. Use when you need specialist knowledge or a particular communication style. |
| **Chain-of-Thought (CoT)** | Instructs the AI to reason step-by-step before giving its final answer. Use for complex decisions, calculations, or analysis. |
| **Few-Shot Examples** | You give the AI two or three examples of the output you want before asking your question. Use when the format or tone is very specific. |
| **Output Priming** | You start the AI's answer for it by writing the first few words of the response you want. Use to force a specific format or opening. |
| **Constraint Pattern** | You add explicit rules the AI must follow (word limit, no jargon, bullet points only). Use when format matters as much as content. |
| **Flipped Interaction** | You ask the AI to interview you with questions instead of giving an answer, so it gathers information before responding. Use for personalised advice. |

---

### 1.2 Hands-On Activity: Persona Pattern

The **persona pattern** is one of the most transformative patterns. By telling the AI WHO it should be, you dramatically change the depth, tone, and focus of its response.

- **Basic prompt (weak):** `"Explain supply chain risks."`
- **Persona prompt (strong):** `"You are a senior supply-chain risk consultant with 20 years of experience advising Fortune 500 companies. Explain the top five supply chain risks facing a mid-sized retail business today. Use plain language suitable for a non-technical board of directors."`

---

> ### 🟩 Try It 1A — Persona Pattern on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> You are a senior supply-chain risk consultant with 20 years of experience
> advising Fortune 500 companies. Explain the top five supply chain risks
> facing a mid-sized retail business today. Use plain language suitable for
> a non-technical board of directors.
> ```
>
> **What to observe:** Notice how the response structures itself with headings, uses business-oriented language, and avoids technical jargon. The persona shapes both the content AND the communication style.

---

> ### 🟩 Try It 1B — Same Persona on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **Prompt to use:**
> ```
> You are a senior supply-chain risk consultant with 20 years of experience
> advising Fortune 500 companies. Explain the top five supply chain risks
> facing a mid-sized retail business today. Use plain language suitable for
> a non-technical board of directors.
> ```
>
> **What to observe:** Compare the response structure, depth, and tone with Claude's answer. Which felt more like a real consultant? Which gave more actionable specifics?

---

### 1.3 Hands-On Activity: Chain-of-Thought (CoT) Pattern

**Chain-of-thought prompting** forces the AI to show its reasoning before committing to a conclusion. This dramatically reduces confident-sounding wrong answers and helps you audit the logic.

---

> ### 🟩 Try It 1C — Chain-of-Thought on Gemini
> **Platform:** Gemini (gemini.google.com)
>
> **Prompt to use:**
> ```
> I am deciding whether to hire a freelancer or a full-time employee for a
> 6-month marketing project. My budget is $40,000. Think through this step
> by step, considering financial, legal, and operational factors, before
> giving me a final recommendation.
> ```
>
> **What to observe:** Watch how Gemini structures its reasoning. Does it identify factors you had not considered? Compare the quality of the recommendation versus a quick one-line answer from a basic prompt.

---

### 1.4 Hands-On Activity: Few-Shot Examples Pattern

When you need a very specific output format, showing the AI two or three examples is far more effective than describing the format in words.

---

> ### 🟩 Try It 1D — Few-Shot Pattern on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **Prompt to use:**
> ```
> Write product descriptions in this style:
>
> Example 1: "Noise-cancelling headphones — Block out the world and hear
> only what matters. 30-hour battery. Built for marathon focus sessions."
>
> Example 2: "Standing desk converter — Turn any desk into a standing desk
> in 10 seconds. Your back will thank you."
>
> Now write a description for: A portable air quality monitor for home use.
> ```
>
> **What to observe:** Notice how the AI mirrors the punchy, benefit-first style you demonstrated. Try removing the examples and asking the same question — the output will be much more generic.

---

> ### 🟧 Module 1 — Reflection Questions
>
> 1. Which pattern felt most immediately useful for your own work? Why?
> 2. Did you notice differences in how Claude, ChatGPT, and Gemini handled the persona pattern?
> 3. When might chain-of-thought reasoning get in the way rather than help?
> 4. How would you combine the persona pattern with the constraint pattern in a single prompt?

---

## Module 2: Semantic Prompting and Contextual Understanding

In this module, you will learn how AI models interpret meaning, not just words. You will practice providing richer context so the AI understands what you really need — not just what you literally said.

### 2.1 What Is Semantic Prompting?

**Semantic prompting** means crafting your request around meaning, intent, and context — not just keywords. AI language models are trained on vast amounts of text and have learned the relationships between ideas, not just word matches.

This means two things for you as a prompt writer:

- The AI can infer a lot from subtle word choices and framing.
- Small changes in how you phrase a question can produce very different answers.
- Providing context about your situation, audience, and goal is more powerful than adding more keywords.

---

### 2.2 Context Variables: The SPACE Framework

A reliable way to build semantic richness into your prompts is to address these five context variables:

| Variable | Questions to answer in your prompt |
|---|---|
| **S — Situation** | What is the background or context of your request? |
| **P — Purpose** | Why do you need this? What will you do with the answer? |
| **A — Audience** | Who will read or use the output? |
| **C — Constraints** | What limits apply? (length, format, tone, what to avoid) |
| **E — Examples** | Can you show any examples of what good looks like? |

> 🟦 **Tip:** You do not need all five in every prompt. Even adding two or three transforms the output from generic to precisely fitted.

---

### 2.3 Hands-On Activity: Context-Poor vs. Context-Rich

Experience the difference context makes by running both versions of the same request.

---

> ### 🟩 Try It 2A — Context-poor prompt on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> Write an email about the project update.
> ```
>
> **What to observe:** Save the response. Notice how generic it is — the AI has to invent the situation, sender, recipient, and purpose.

---

> ### 🟩 Try It 2B — Context-rich prompt on Claude *(new conversation)*
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> Situation: I am a project manager at a software company. Our Q3 product
> launch has been delayed by two weeks due to a vendor issue.
>
> Purpose: I need to inform my key client (a non-technical VP of Operations)
> of the delay without causing panic.
>
> Audience: A busy executive who values brevity and wants to know the impact
> on their business, not technical details.
>
> Constraint: Maximum 150 words, professional but warm tone, end with a
> clear next step.
>
> Write the email.
> ```
>
> **What to observe:** Compare this with Try It 2A. The same AI produces a completely different — and far more usable — output simply because you supplied semantic context.

---

### 2.4 Understanding Framing Effects

The frame you put around a question changes what the AI considers relevant. This is one of the most underappreciated skills in prompt engineering.

**Example:** All three prompts below ask about remote work, but they frame it differently:

- `"What are the benefits of remote work?"` — frames it as a **positive inquiry**
- `"What are the hidden risks of remote work that managers underestimate?"` — frames it as a **risk audit**
- `"You are writing a balanced briefing paper for a CEO who is undecided. Assess remote work."` — frames it as **neutral analysis for a decision-maker**

---

> ### 🟩 Try It 2C — Framing on Gemini
> **Platform:** Gemini (gemini.google.com)
>
> **Prompt to use:**
> ```
> You are writing a balanced briefing paper for a CEO who is currently
> undecided about whether to make the company's remote work policy permanent.
> Assess the evidence on both sides. Be specific. Conclude with a clear
> recommendation and the one biggest risk of each choice.
> ```
>
> **What to observe:** Compare the output depth versus simply asking "What do you think about remote work?" The framing signals your purpose, desired output type (briefing paper), audience (CEO), and the kind of conclusion you need.

---

### 2.5 Negative Space Prompting

**Negative space prompting** means telling the AI what NOT to do. This is surprisingly powerful because it removes assumptions the AI would otherwise make by default.

---

> ### 🟩 Try It 2D — Negative constraints on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **Prompt to use:**
> ```
> Give me five creative team-building activities for a remote team of 12
> people. Do NOT suggest anything involving video calls, quizzes, or online
> games. Do NOT suggest activities that cost money. Do NOT give generic
> ideas like "virtual coffee chats." Each idea must be genuinely novel.
> ```
>
> **What to observe:** The negative constraints force the AI out of its default patterns and into genuinely creative territory. Without them, you would almost certainly receive the five most common suggestions.

---

> ### 🟧 Module 2 — Reflection Questions
>
> 1. Which of the SPACE variables do you most often forget to include in your daily AI prompts?
> 2. Try writing a context-rich prompt for something you use AI for regularly at work. What changed?
> 3. When could negative space prompting backfire? *(Hint: think about over-constraining the output)*
> 4. Did Claude, ChatGPT, and Gemini differ in how much context they needed before giving useful output?

---

## Module 3: Multimodal Prompts

In this module, you will learn to combine text with images in your prompts — a capability available in ChatGPT (with GPT-4o), Claude, and Gemini. Multimodal prompting dramatically expands what you can do with AI without any coding or technical setup.

### 3.1 What Does Multimodal Mean?

**Multimodal** refers to using more than one type of input in a single prompt. In practice, this means combining:

- Text + Images (photograph, diagram, chart, screenshot)
- Text + Documents (PDF, spreadsheet — in some platforms)
- Text + Audio or Video (in some advanced platforms)

This lab focuses on the most universally accessible combination: **text and images**. You can upload images directly in the chat interface of all three platforms — no account upgrades required for basic image prompting.

---

### 3.2 How to Upload an Image in Each Platform

| Platform | How to attach an image |
|---|---|
| **ChatGPT** | Click the paperclip icon (left of the message box) or drag an image into the chat window. |
| **Claude** | Click the paperclip or image icon below the message input field. Drag and drop also works. |
| **Gemini** | Click the image icon (looks like a landscape photo) in the toolbar above the message box. |

> 🟦 **Tip: What images work well for these exercises?**
> - A photo of a product, workplace, or everyday object
> - A screenshot of a document, email, or spreadsheet
> - A chart or graph from a report
> - A handwritten note or whiteboard photo
> - A marketing ad or social media post screenshot

---

### 3.3 Hands-On Activity: Image Description and Analysis

The most fundamental multimodal skill is getting the AI to accurately describe, interpret, and analyse an image you provide.

> 📷 **Before you start:** Find or take a photograph of any workplace scene — your desk, a meeting room, a product, or a printed document. A simple smartphone photo works perfectly.

---

> ### 🟩 Try It 3A — Detailed image analysis on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> [Upload your image]
>
> Analyse this image in detail. Describe what you see, identify any text
> present, and tell me three things a business professional might find
> notable or useful about what is shown.
> ```
>
> **What to observe:** Notice how Claude goes beyond simple description into interpretation and business relevance. The text instruction shapes what the AI pays attention to in the image.

---

> ### 🟩 Try It 3B — Structured image report on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **Prompt to use:**
> ```
> [Upload the same image]
>
> You are a business analyst reviewing this image. Produce a structured
> report with three sections: (1) What is shown, (2) Key observations,
> (3) Recommended actions based on what you see. Be specific and professional.
> ```
>
> **What to observe:** The structured format instruction produces a report-style output rather than a paragraph. Compare the usability of this format versus the free-text response from Claude.

---

### 3.4 Hands-On Activity: Data Extraction from Images

One of the most practical uses of multimodal prompts is extracting structured data from photos of tables, handwritten notes, or printed documents.

> 📷 **Before you start:** Take a photo of any table of information — a printed schedule, a handwritten list, a restaurant menu, a price list, or any similar document.

---

> ### 🟩 Try It 3C — Data extraction on Gemini
> **Platform:** Gemini (gemini.google.com)
>
> **Prompt to use:**
> ```
> [Upload a photo of a table or list]
>
> Extract all the information from this image and present it as a clean,
> organised table. If there are any numbers, double-check them. If any
> text is unclear, indicate that with [unclear].
> ```
>
> **What to observe:** The `[unclear]` instruction is an example of negative space prompting combined with multimodal — you are telling the AI how to handle uncertainty rather than letting it guess.

---

### 3.5 Hands-On Activity: Creative Interpretation

Multimodal prompts are not limited to analysis. You can use images as creative starting points.

---

> ### 🟩 Try It 3D — Creative brief from an image on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> [Upload a photo of an outdoor scene, a product, or any interesting visual]
>
> Imagine you are a marketing copywriter. Based ONLY on what you see in
> this image, write a punchy 50-word advertising tagline and a three-sentence
> product description for a fictional product this scene could represent.
> Be creative and specific.
> ```
>
> **What to observe:** This exercise shows how you can use an image as creative raw material rather than as a document to be analysed. The AI interprets visual mood, composition, and context to generate original copy.

---

### 3.6 Multimodal Prompt Design Principles

| Principle | Why it matters |
|---|---|
| **Always add a text instruction** | Images alone produce generic descriptions. Your text shapes what the AI focuses on. |
| **Specify the output format** | Tell the AI how you want the result: table, bullet points, paragraph, report, etc. |
| **State your purpose** | Why are you analysing this image? This changes what the AI considers relevant. |
| **Use the persona pattern** | Combining "You are a [role]" with an image produces expert-level analysis. |
| **Ask about uncertainty** | Request that the AI flag anything it cannot read or is unsure about. |

---

> ### 🟧 Module 3 — Reflection Questions
>
> 1. Which multimodal use case is most immediately applicable to your own work?
> 2. Did you notice differences in how accurately the three platforms read text from images?
> 3. What types of images might AI models struggle with, and how could you compensate in your text prompt?
> 4. How could you combine image analysis with the chain-of-thought pattern from Module 1?

---

## Module 4: Iterative Prompt Refinement Techniques

In this module, you will learn one of the most important — and most overlooked — skills in prompt engineering: treating a conversation with an AI as an iterative design process, not a single transaction.

### 4.1 Why Iteration Matters

Most people use AI in a one-shot mode: ask a question, get an answer, accept it or discard it. Expert prompt engineers treat the first response as a **first draft** — the beginning of a dialogue.

Iterative refinement works because:

- Each response gives you information about how the AI understood your request.
- You can steer, correct, and expand the output without starting over.
- The AI accumulates context about your preferences as the conversation grows.
- Complex outputs (reports, plans, analyses) are almost always built across multiple exchanges.

---

### 4.2 The Refinement Toolkit: Seven Techniques

| Technique | What you say and when to use it |
|---|---|
| **Redirect** | *"That is not quite what I meant. What I actually need is..."* — Use when the AI misunderstood your intent. |
| **Zoom In** | *"Focus specifically on [one part]. Go much deeper on that aspect only."* — Use to get detail on one element. |
| **Zoom Out** | *"Step back and give me a higher-level view of this topic for a general audience."* — Use when too much detail is overwhelming. |
| **Reformat** | *"Rewrite that as a table / bullet list / executive summary / one paragraph."* — Use when the structure does not suit your purpose. |
| **Raise the Bar** | *"Good start. Now make it 30% shorter, remove all jargon, and add one concrete real-world example."* — Use to push quality higher. |
| **Perspective Shift** | *"Now argue the opposite position."* or *"Rewrite this from the perspective of a skeptical customer."* — Use to stress-test ideas. |
| **Transfer Style** | *"Rewrite this in the style of a Harvard Business Review article / a casual blog post / a formal legal brief."* — Use to match communication context. |

---

### 4.3 Hands-On Activity: The Refinement Chain

In this exercise you will build a complete output through **five rounds of iterative refinement** — starting from a weak prompt and finishing with something polished and specific.

> 🟦 **Scenario:** You are preparing a one-page brief on the business case for investing in employee well-being programs. Your audience is a cost-conscious CFO who is skeptical about "soft" initiatives. You will start with a bad prompt and refine it to excellence in five steps.

---

#### Round 1 — The weak starting prompt

> ### 🟩 Try It 4A — Start weak (Claude)
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> Tell me about employee well-being.
> ```
>
> **What to observe:** Save this response. Notice it is generic, not targeted at a CFO, has no business case framing, and is probably too long or too short for a one-page brief.

---

#### Round 2 — Add audience and purpose

> ### 🟩 Try It 4B — Redirect and add context *(continue same conversation)*
> **Platform:** Claude (claude.ai) — continue the same conversation
>
> **Prompt to use:**
> ```
> That is too general. I need a business case specifically for a CFO who
> is skeptical about investing in employee well-being programs. Focus on
> measurable ROI and cost implications. What does the evidence say?
> ```
>
> **What to observe:** The response should now shift toward financial metrics, turnover costs, productivity data, and measurable outcomes. Notice how the AI uses the context from the previous exchange.

---

#### Round 3 — Zoom in on the strongest argument

> ### 🟩 Try It 4C — Zoom In *(continue same conversation)*
> **Platform:** Claude (claude.ai) — continue the same conversation
>
> **Prompt to use:**
> ```
> The point about reduced absenteeism and turnover costs is the most
> compelling for my CFO. Zoom in on that specifically. Give me three
> concrete statistics or case studies with real numbers that I can cite.
> ```
>
> **What to observe:** You are now directing the AI like an editor directing a researcher. The conversation history means Claude knows your context and purpose — you do not need to repeat it.

---

#### Round 4 — Reformat for the deliverable

> ### 🟩 Try It 4D — Reformat *(continue same conversation)*
> **Platform:** Claude (claude.ai) — continue the same conversation
>
> **Prompt to use:**
> ```
> Now restructure everything we have developed into a one-page executive
> brief. Use this structure: (1) The Business Problem, (2) The Evidence,
> (3) Financial Impact, (4) Recommended Action. Use plain business language.
> Maximum 300 words.
> ```
>
> **What to observe:** The AI draws on the entire conversation — the statistics, the CFO framing, the specific focus areas — and organises it into the format you need.

---

#### Round 5 — Raise the bar

> ### 🟩 Try It 4E — Raise the Bar *(continue same conversation)*
> **Platform:** Claude (claude.ai) — continue the same conversation
>
> **Prompt to use:**
> ```
> Good. Now do two things: (1) Make the opening sentence so compelling
> that a busy CFO would not stop reading. (2) Add one line in the
> Recommended Action section that pre-empts the most obvious objection
> a CFO would raise.
> ```
>
> **What to observe:** This final refinement shows the power of iterative prompting — you are now doing editorial direction, not just prompting. Compare the final output with your Round 1 response. The transformation is significant.

---

### 4.4 Cross-Platform Refinement Comparison

> ### 🟩 Try It 4F — Refinement on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **What to do:** Start a new conversation. Use the same five-round refinement sequence (4A through 4E) on ChatGPT. Run the exact same prompts in sequence.
>
> **What to observe:** Compare the final outputs from Claude and ChatGPT. Which platform produced the more polished executive brief? Which handled the "raise the bar" instruction better? Which held context more effectively across five rounds?

---

### 4.5 Meta-Prompting: Ask the AI to Improve Your Prompt

One of the most powerful iterative techniques is to ask the AI itself to critique and improve your prompt before you even submit your real request.

---

> ### 🟩 Try It 4G — Meta-prompting on Gemini
> **Platform:** Gemini (gemini.google.com)
>
> **Prompt to use:**
> ```
> I am going to give you a prompt I want to send to an AI. Before I send
> it, I want you to: (1) Identify what is unclear or missing, (2) Suggest
> how to improve it, (3) Write an improved version.
>
> Here is my prompt: "Help me write a better presentation."
> ```
>
> **What to observe:** Gemini will analyse your weak prompt and produce a dramatically stronger version. This meta-prompting technique is a fast track to better results — especially when you are not sure how to frame a complex request.

---

> ### 🟧 Module 4 — Reflection Questions
>
> 1. Which of the seven refinement techniques do you think will be most useful in your daily work?
> 2. After running the five-round refinement chain, what surprised you most about how the output evolved?
> 3. Did Claude, ChatGPT, and Gemini differ in how well they maintained context across multiple exchanges?
> 4. When might iterative refinement be a waste of time compared to writing one strong prompt upfront?
> 5. How would you teach the refinement chain to a colleague who is new to AI tools?

---

## Lab Summary & Quick-Reference Cheat Sheet

### Key Takeaways by Module

| Module | The single most important thing to remember |
|---|---|
| **1 — Advanced Patterns** | Choose a pattern before you write. Persona + CoT + Constraint combined in one prompt produces expert-level, structured output. |
| **2 — Semantic Prompting** | Context is everything. SPACE (Situation, Purpose, Audience, Constraints, Examples) transforms a generic answer into a precise one. |
| **3 — Multimodal Prompts** | Images alone produce generic output. Your text instruction shapes what the AI looks for, how it interprets, and what format it returns. |
| **4 — Iterative Refinement** | Treat your first response as a first draft. Use the seven refinement techniques to direct, deepen, and polish like an editor. |

---

### Platform Comparison Summary

| Capability | ChatGPT vs Claude vs Gemini — general observations |
|---|---|
| **Persona Pattern** | All three handle it well. Claude tends to maintain persona consistency longest in extended conversations. |
| **Chain-of-Thought** | All three respond well. ChatGPT's reasoning can be very explicit; Claude's tends to be more narrative. |
| **Image Analysis** | All three are capable. Gemini often performs strongly on document photos; Claude handles nuanced interpretation well. |
| **Long Conversations** | Claude and ChatGPT maintain context across long refinement chains reliably. Gemini may need occasional context reminders. |
| **Creative Tasks** | All three are strong. Claude tends toward structured creativity; ChatGPT and Gemini often take more unexpected creative directions. |

---

### The Master Prompt Template

Use this template when you need a high-quality result and want to apply multiple techniques at once:

```
ROLE: You are [specific expert role with years of experience and relevant context].

SITUATION: [Background context — what is happening and why this matters].

TASK: [Exactly what you want produced — be specific about scope].

AUDIENCE: [Who will read this — their role, knowledge level, and what they care about].

FORMAT: [Structure, length, tone, and any specific sections required].

CONSTRAINTS: Do NOT [list 2–3 things to avoid]. DO [list 1–2 things to ensure].

REASONING: Think through this step by step before writing your final response.
```

---

## Glossary of Key Terms

| Term | Plain-language definition |
|---|---|
| **Prompt** | The message or instruction you send to an AI chatbot. |
| **Prompt Pattern** | A reusable template or structure for crafting prompts that produces predictable, high-quality results. |
| **Persona Pattern** | Instructing the AI to adopt a specific expert role or identity. |
| **Chain-of-Thought** | Instructing the AI to reason step-by-step before giving its final answer. |
| **Few-Shot Prompting** | Providing two or three examples in your prompt to show the AI the format or style you want. |
| **Semantic Prompting** | Crafting prompts around meaning, intent, and context rather than just keywords. |
| **Negative Space Prompting** | Telling the AI explicitly what NOT to do to push it toward more creative or specific output. |
| **Multimodal Prompt** | A prompt that combines text with one or more other input types, such as images. |
| **Iterative Refinement** | The practice of treating an AI conversation as a multi-step design process, building toward a polished result. |
| **Meta-Prompting** | Asking the AI to evaluate and improve your prompt before you submit your actual request. |
| **Output Priming** | Starting the AI's answer for it by writing the first few words of the response you want. |

---

## Contributing

Found a better prompt? Want to add a module? PRs are welcome. Please keep exercises platform-agnostic (ChatGPT / Claude / Gemini) and suitable for non-technical learners.

## License

This lab guide is released under the [MIT License](LICENSE). Free to use, adapt, and share.
