# 📋 Application-Oriented Prompt Engineering — Hands-On Lab

> **Self-paced lab** | No coding required 
>
> Practice directly in [ChatGPT](https://chat.openai.com) · [Claude](https://claude.ai) · [Gemini](https://gemini.google.com)

---

## 📖 How to Use This Lab Guide

This lab is self-paced. Each module opens with a short concept explanation followed by colour-coded exercises. Work through them in order and take notes after each exercise — the reflection questions are designed to deepen understanding, not just test recall.

| Icon / Box | What it means |
|---|---|
| 🟩 **Try It box** | A live exercise: copy the prompt and run it in the specified chatbot right now |
| 🟧 **Reflection box** | Discussion or journaling questions to consolidate what you have just done |
| 🟦 **Info box** | Key concepts, tips, and important background knowledge |
| 🟪 **Step box** | A guided walkthrough of a multi-step process (Custom GPTs and Gems) |
| 🟥 **Caution box** | Common mistakes to watch for and how to avoid them |

---

## Table of Contents

- [Module 1: Customizing Prompts for Different LLM Platforms](#module-1-customizing-prompts-for-different-llm-platforms)
- [Module 2: Optimizing Prompts for Specific LLMs](#module-2-optimizing-prompts-for-specific-llms)
- [Module 3: Information Extraction Strategies](#module-3-information-extraction-strategies)
- [Module 4: Custom GPTs and Gemini Gems](#module-4-custom-gpts-and-gemini-gems)
- [Lab Summary & Cheat Sheet](#lab-summary-cheat-sheet-and-next-steps)
- [Glossary](#glossary-of-key-terms)

---

## Module 1: Customizing Prompts for Different LLM Platforms

ChatGPT, Claude, and Gemini are each trained differently, have different strengths, and respond differently to the same prompt. In this module you will learn what makes each platform unique and how to write prompts that play to those strengths.

### 1.1 Platform Personalities: What Each LLM Does Best

Think of the three platforms as different kinds of expert colleagues:

| Platform | Character | Strongest at | Watch out for |
|---|---|---|---|
| **ChatGPT (GPT-4o)** | Versatile all-rounder | Broad knowledge, structured outputs, plugin integrations, code | Can be overconfident; sometimes verbose without prompting for brevity |
| **Claude** | Thoughtful analyst | Long documents, nuanced reasoning, careful instruction-following, safety-aware responses | Can be overly cautious; may hedge more than needed on straightforward questions |
| **Gemini** | Google-connected generalist | Real-time web information, Google Workspace integration, multimodal tasks | Can prioritise recency over depth; responses sometimes shallower on niche topics |

---

### 1.2 The Three Customization Levers

Regardless of which platform you use, you have three levers to adjust your prompt for that platform:

- **Tone lever** — how formal, direct, or conversational your language is
- **Instruction lever** — how explicit you are about format, length, and structure
- **Context lever** — how much background information you provide upfront

> 🟦 **Key insight:** Claude responds best when the instruction lever is turned up high (very explicit instructions). ChatGPT handles moderate instruction levels well. Gemini often benefits most from turning up the context lever.

---

### 1.3 Hands-On Activity: Same Task, Three Platforms

In this exercise you will send the same core request to all three platforms and observe how the outputs differ. Then you will customise the prompt for each platform and compare the improvement.

#### Round A — The Generic Prompt

Send the same prompt to all three platforms and compare the results.

---

> ### 🟩 Try It 1A — Generic prompt on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **Prompt to use:**
> ```
> Write a short report on the impact of artificial intelligence on the job market.
> ```
>
> **What to observe:** Note the structure, length, tone, and depth. Save or copy this response before moving on.

---

> ### 🟩 Try It 1B — Generic prompt on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> Write a short report on the impact of artificial intelligence on the job market.
> ```
>
> **What to observe:** Compare with ChatGPT: Does Claude use more or fewer headings? Is the language more cautious? Is the length similar?

---

> ### 🟩 Try It 1C — Generic prompt on Gemini
> **Platform:** Gemini (gemini.google.com)
>
> **Prompt to use:**
> ```
> Write a short report on the impact of artificial intelligence on the job market.
> ```
>
> **What to observe:** Does Gemini include more recent examples or data? Is the tone different? How does the report structure compare to the other two?

---

#### Round B — Platform-Customized Prompts

Now rerun the task with prompts tailored to each platform's strengths.

---

> ### 🟩 Try It 1D — ChatGPT-optimised prompt
> **Platform:** ChatGPT (chat.openai.com) — new conversation
>
> **Prompt to use:**
> ```
> You are a senior economics journalist writing for a business magazine.
> Write a 400-word report on the impact of AI on the job market. Structure
> it with: (1) an opening hook, (2) two specific job categories being
> disrupted, (3) two job categories being created, (4) a balanced
> conclusion. Be specific — cite real industry examples. No jargon.
> ```
>
> **What to observe:** Compare this with Try It 1A. The added role, structure, length, specificity, and example instructions unlock ChatGPT's full capability.

---

> ### 🟩 Try It 1E — Claude-optimised prompt
> **Platform:** Claude (claude.ai) — new conversation
>
> **Prompt to use:**
> ```
> I need a nuanced, carefully reasoned analysis of AI's impact on employment.
> Please do the following: First, acknowledge the genuine complexity and
> uncertainty in this area. Second, present the strongest evidence for job
> displacement with specific sectors. Third, present the strongest evidence
> for job creation and transformation. Fourth, identify what we genuinely
> do not know yet. Fifth, write a conclusion that does not oversimplify.
> Audience: educated non-specialist readers. Length: 450–500 words.
> ```
>
> **What to observe:** Claude responds excellently to explicit multi-step instructions and requests for nuance. Notice how the word "nuanced" and "what we do not know" shapes the response differently from a generic prompt.

---

> ### 🟩 Try It 1F — Gemini-optimised prompt
> **Platform:** Gemini (gemini.google.com) — new conversation
>
> **Prompt to use:**
> ```
> Using the most current available information, write a 350-word briefing
> on how AI is changing the job market. Focus on developments from the past
> 12–18 months. Include specific companies, announcements, or research
> findings where possible. Audience: a business executive who follows
> technology news but is not a technical specialist. Format: short
> paragraphs, no bullet points.
> ```
>
> **What to observe:** Gemini's connection to current information is a genuine advantage. The "past 12–18 months" and "specific companies" instructions direct it toward its strength.

---

### 1.4 Platform-Specific Customization Rules

| Customization element | ChatGPT | Claude | Gemini |
|---|---|---|---|
| **Role/Persona** | Responds strongly — always add a role | Responds strongly — add role + expertise level | Responds moderately — useful but less transformative |
| **Explicit structure** | Moderate impact — numbered lists help | High impact — numbered instructions work best | Moderate impact — paragraph format often preferred |
| **Length instruction** | Usually follows well | Follows very precisely — be exact | Approximate — may exceed or fall short slightly |
| **Recency/current info** | Limited unless browsing enabled | Limited to training data | Strong — explicit "recent" instructions unlock this |
| **Tone instruction** | Responds well to any tone | Responds well but defaults to measured | Responds well but defaults to conversational |
| **Negative constraints** | Useful | Very useful — highly instruction-compliant | Useful but may need reinforcing |

---

> ### 🟧 Module 1 — Reflection Questions
>
> 1. Which platform produced the most immediately usable output on the generic prompt (1A–1C)?
> 2. After customizing your prompts in Round B, which platform showed the biggest improvement from its generic version?
> 3. For your own most common use of AI, which platform's characteristics fit best — and what one customization would improve your prompts today?
> 4. Did you notice any cases where a platform ignored part of your instruction? Which part was ignored and why might that be?

---

## Module 2: Optimizing Prompts for Specific LLMs

Optimization goes beyond basic customization. In this module you will learn platform-specific techniques that significantly improve output quality: how to use system-level instructions, how to manage context length, how to handle refusals, and how to get consistent formatting.

### 2.1 Understanding How Each LLM Processes Instructions

> 🟦 **How the three platforms process your prompts**
>
> **ChatGPT** — Treats your message as a conversation turn. It balances following instructions with being helpful and engaging. It sometimes takes creative liberties with format if you do not specify.
>
> **Claude** — Treats instructions almost like a contract. If you say "do exactly these five things in this order," it usually does. This makes it the most reliably controllable platform for structured outputs.
>
> **Gemini** — Treats your message as a query. It draws on Google Search patterns, so prompts that read more like a focused research request often work well.

---

### 2.2 The CRAFT Optimization Framework

CRAFT is a practical checklist for optimizing any prompt for any platform. Run through it before sending a complex or high-stakes prompt:

| Letter | Element | Key question to ask yourself |
|---|---|---|
| **C** | Context | Have I given the AI enough background to understand my situation? |
| **R** | Role | Have I told the AI who it should be (expert role, perspective, audience awareness)? |
| **A** | Action | Have I stated the task with a precise, active verb (write, analyse, compare, summarise)? |
| **F** | Format | Have I specified structure, length, tone, and what sections or elements I expect? |
| **T** | Tone/Target | Have I stated the intended audience and the tone appropriate for them? |

---

### 2.3 Hands-On Activity: CRAFT Optimization in Practice

**Starting prompt (weak):** `"Tell me about the risks of outsourcing."`

---

> ### 🟩 Try It 2A — CRAFT-optimized prompt on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> Context: I am the operations director of a 120-person software company
> considering outsourcing our customer support function to a third-party
> provider in Eastern Europe.
>
> Role: You are a senior operations consultant who has advised 50+ companies
> on outsourcing decisions.
>
> Action: Analyse the five most significant risks of this outsourcing
> decision and provide a mitigation strategy for each risk.
>
> Format: Use a two-column structure — Risk in the first column, Mitigation
> in the second. Then add a brief overall recommendation paragraph.
>
> Tone: Direct and practical, written for an experienced executive who does
> not need basic definitions.
> ```
>
> **What to observe:** Compare the output depth, relevance, and usability with the weak starting prompt. Count how many CRAFT elements transformed the response.

---

### 2.4 Managing Context Window and Memory

A "context window" is the amount of text the AI can hold in its "working memory" during a conversation.

| Platform | Context window (approx.) | Practical implication |
|---|---|---|
| **ChatGPT (GPT-4o)** | Very large (128K tokens ≈ 300 pages) | Can handle very long conversations; paste long documents freely |
| **Claude** | Very large (200K tokens ≈ 450 pages) | Excellent for long documents and extended multi-step projects |
| **Gemini** | Large (1M tokens — Gemini 1.5) | Can handle extremely long inputs; strong with long documents |

> 🟦 **Context management tips that apply to all platforms**
> - Summarize earlier parts of a long conversation if the AI starts losing track: *"Here is a summary of what we have agreed so far: [summary]. Now continue with..."*
> - For long documents, paste the document first, then ask your question.
> - Start a new conversation when switching to a completely different topic.
> - In very long conversations, explicitly remind the AI of critical constraints: *"Remember: this is for a non-technical audience"*

---

### 2.5 Handling Platform Refusals and Guardrails

> 🟥 **Important: Legitimate workarounds only**
> The techniques below are for getting better results on legitimate professional and educational tasks. Never attempt to bypass safety features for genuinely harmful purposes. If a platform consistently refuses a legitimate professional request, try rephrasing the context rather than removing safety guardrails.

| Situation | Why it happens | How to address it legitimately |
|---|---|---|
| Overly cautious medical/legal content | Platform adds disclaimers to avoid liability | Add: *"I understand this is general information only and I will consult a professional for decisions."* |
| Refuses competitive analysis | Prompt sounds like it may be used for manipulation | Add: *"This is for an internal strategy presentation, not for external publication."* |
| Strips out specific details | Platform detects potential sensitivity in topic | Reframe: add your professional context and the purpose of the information upfront |
| Generic answer to a sensitive question | Default safety mode triggered | Provide more specific professional context in the opening of your prompt |

---

> ### 🟩 Try It 2B — Context reframing on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **Prompt to use:**
> ```
> I am an HR manager preparing a training session for our management team
> on recognising signs of employee burnout. For this training, list the
> 8 most common behavioural and performance indicators of burnout that a
> manager might observe in a team member, with a brief note on how to
> approach each sensitively.
> ```
>
> **What to observe:** The professional context (HR manager, training purpose, management audience) ensures the AI treats this as a legitimate workplace request rather than triggering generic mental health disclaimers.

---

### 2.6 Getting Consistent Formatting Across Sessions

Use these techniques to lock in consistent formatting:

- **Use labelled sections:** `"Use these exact section headings: [Section 1], [Section 2], [Section 3]"`
- **Specify element counts:** `"Give exactly 5 bullet points, each no longer than one sentence"`
- **Show a skeleton:** Paste a blank template and say `"Fill in this template"`
- **Use "Output only":** `"Output only the formatted result. Do not add any introduction or closing remarks."`

---

> ### 🟩 Try It 2C — Template-locked output on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> Fill in the following meeting summary template based on this scenario:
> [A 1-hour product roadmap meeting where the team agreed to delay Feature X
> by 6 weeks, prioritise a mobile bug fix, and schedule a customer feedback
> session for next Friday.]
>
> Template to fill:
> Meeting: [Meeting name]
> Date: [Date]
> Key Decisions:
> 1. [Decision]
> 2. [Decision]
> 3. [Decision]
> Action Items:
> - [Owner] will [Action] by [Date]
> - [Owner] will [Action] by [Date]
> Next Meeting: [Details]
> ```
>
> **What to observe:** The template locks the structure completely. Claude is highly instruction-compliant and will mirror the template format precisely. Try this with a real meeting scenario for an immediately useful output.

---

> ### 🟧 Module 2 — Reflection Questions
>
> 1. Which element of CRAFT do you most often skip in your everyday prompts?
> 2. Have you ever received an overly cautious or hedged response from an AI? After this module, how would you rephrase that prompt?
> 3. Which platform do you find most consistently follows your formatting instructions?
> 4. Think of a repetitive task you do at work. How could you create a template prompt that gives you a consistent, usable output every time?

---

## Module 3: Information Extraction Strategies

One of the most practically valuable applications of prompt engineering is extracting specific, structured information from messy, long, or complex sources. In this module you will learn how to turn raw text into clean, usable data — without any spreadsheet formulas or coding.

### 3.1 What Is Information Extraction?

Information extraction means taking unstructured text — an email thread, a report, a contract, a customer review, a meeting transcript — and pulling out specific facts, patterns, or summaries in a format you can actually use.

| Extraction type | What you are pulling out | Common source |
|---|---|---|
| **Entity extraction** | Names, dates, places, organisations, amounts | Contracts, emails, reports |
| **Sentiment extraction** | Positive, negative, neutral tone; emotional signals | Customer reviews, feedback, social media |
| **Summary extraction** | Key points, decisions, action items | Meeting notes, long reports, articles |
| **Structured data extraction** | Tables, lists, categorised data from prose | Research papers, product descriptions, invoices |
| **Comparison extraction** | Similarities and differences across multiple texts | Competitor content, multiple reports |
| **Pattern extraction** | Recurring themes, trends, anomalies | Survey responses, log files, communications |

---

### 3.2 The Extraction Prompt Formula

> 🟦 **Four-part extraction prompt formula**
>
> **Part 1 — SOURCE:** Paste the text you want to extract from, or tell the AI where it is.
>
> **Part 2 — TARGET:** Tell the AI exactly what you want extracted (entities, dates, themes, sentiment, etc.).
>
> **Part 3 — FORMAT:** Tell the AI how to present the extracted information (table, numbered list, JSON, bullet points).
>
> **Part 4 — HANDLING:** Tell the AI what to do when information is missing, unclear, or ambiguous.

---

### 3.3 Hands-On Activity: Entity Extraction

Use this sample text for the exercises below, or substitute a real email or document you have at hand.

> 📄 **Sample text for extraction exercises (copy this):**
> *"Following our meeting on 14 March, I wanted to confirm the key points we discussed. Priya Sharma from Nexatech will lead the integration project with a budget of $240,000, targeting completion by 30 September. David Wu from our legal team will review the vendor contract by 28 March. The main risk identified was the dependency on the API delivery from Cloudburst Inc., which Raj Patel is chasing. Our next review call is scheduled for 4 April at 2pm GMT. Please confirm attendance with Sarah Okonkwo who is coordinating the calendar invites."*

---

> ### 🟩 Try It 3A — Entity extraction on ChatGPT
> **Platform:** ChatGPT (chat.openai.com)
>
> **Prompt to use:**
> ```
> Extract all structured information from the text below and present it as
> a clean table with five columns: Person Name, Organisation/Role, Task or
> Responsibility, Deadline or Date, and Amount (if any). If a field is not
> mentioned, write "not stated".
>
> Text: [paste the sample text above]
> ```
>
> **What to observe:** ChatGPT will produce a clean table even from dense prose. Check accuracy — did it capture all six people? Did it correctly attribute tasks and dates?

---

### 3.4 Hands-On Activity: Sentiment and Theme Extraction

> 📄 **Sample customer feedback for sentiment exercise (copy this):**
> *"I have been a customer for three years and generally the service has been excellent. However, the most recent product update completely changed the navigation and I genuinely cannot find features I use every day. I spent 45 minutes on hold trying to get help and the agent, while friendly, could not resolve the issue. I still like the product overall but I am seriously considering switching if the navigation is not fixed or if there is not a way to revert to the old layout. The price increase last quarter did not help either."*

---

> ### 🟩 Try It 3B — Structured sentiment analysis on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> Analyse the customer feedback below and extract the following, presenting
> each as a labelled section:
>
> 1. Overall sentiment score (1–5 where 1 = very negative, 5 = very
>    positive) with a one-sentence justification
> 2. Positive elements mentioned (bullet list)
> 3. Negative elements mentioned (bullet list)
> 4. Churn risk level (Low / Medium / High) with reasoning
> 5. Top recommended action for the customer success team (one sentence)
>
> Feedback: [paste the sample feedback above]
> ```
>
> **What to observe:** Claude's careful instruction-following is ideal for this structured analysis. Notice how specifying numbered sections, a scoring system, and a recommendation produces an immediately actionable output rather than just a summary paragraph.

---

> ### 🟩 Try It 3C — Cross-feedback pattern extraction on Gemini
> **Platform:** Gemini (gemini.google.com)
>
> **Prompt to use:**
> ```
> You are a customer insights analyst. I will give you three customer
> reviews. After reading all three, identify: (1) the top two themes that
> appear across multiple reviews, (2) any contradictions between the
> reviews, (3) the single most urgent issue to address based on the
> combined feedback.
>
> Review 1: "Great product but delivery was two weeks late and the
> packaging was damaged."
>
> Review 2: "Love the quality but shipping always takes longer than stated
> on the website."
>
> Review 3: "The product itself is excellent. However this is the second
> time my order arrived late. Customer service was apologetic but offered
> no solution."
> ```
>
> **What to observe:** This exercise shows cross-document pattern extraction. Gemini identifies that delivery reliability is the dominant theme across all three — a conclusion you could not draw from reading just one review.

---

### 3.5 Hands-On Activity: Document Summary Extraction

> ### 🟩 Try It 3D — Structured document summary on Claude
> **Platform:** Claude (claude.ai)
>
> **Prompt to use:**
> ```
> I will paste a block of text. Extract the following in this exact format:
>
> THE CORE ARGUMENT (one sentence):
> KEY EVIDENCE (3 bullet points):
> IMPLICATIONS FOR A BUSINESS DECISION-MAKER (2 bullet points):
> WHAT IS MISSING OR UNCERTAIN (1 bullet point):
> ACTION RECOMMENDED (one sentence):
>
> Text: [Paste any article, report section, or long email you have at hand]
> ```
>
> **What to observe:** The "what is missing" and "uncertainty" instruction is an advanced extraction technique. It forces the AI to think critically rather than just summarise positively. Excellent for research or due diligence contexts.

---

### 3.6 Advanced: Chained Extraction

Chained extraction means performing multiple extraction steps in sequence, each building on the last.

> 🟦 **Chained extraction sequence for a contract or long report**
>
> **Step 1** — Ask for a plain-language summary of what the document covers.
>
> **Step 2** — Ask for all dates, parties, and obligations extracted as a table.
>
> **Step 3** — Ask: *"Based on the above, what are the three highest-risk clauses or commitments for [your organisation]?"*
>
> **Step 4** — Ask: *"Draft three questions a lawyer should clarify before signing."*
>
> This four-step chain turns a dense document into a decision-ready briefing — in minutes, not hours.

---

> ### 🟩 Try It 3E — Chained extraction on ChatGPT
> **Platform:** ChatGPT (chat.openai.com) — use a single conversation for all four messages
>
> **Message 1:**
> ```
> Read the following text and give me a plain-language summary in 3
> sentences: [paste any policy document, terms of service excerpt, or
> report section]
> ```
>
> **Message 2** *(after response):*
> ```
> Now extract all named parties, obligations, deadlines, and amounts from
> the same text as a table.
> ```
>
> **Message 3** *(after response):*
> ```
> Based on everything above, what are the two biggest risks or obligations
> for someone agreeing to these terms?
> ```
>
> **Message 4** *(after response):*
> ```
> Draft two clarifying questions I should ask before committing.
> ```
>
> **What to observe:** Run all four messages in sequence in one conversation. Watch how each step builds on the previous. The final output — a risk summary and clarifying questions — would take an analyst significant time to produce manually.

---

### 3.7 Extraction Accuracy: Verification Techniques

> 🟥 **Always verify extracted data before using it for decisions**
> AI extraction is fast and useful, but not perfect. Always spot-check extracted tables against the source text. Numbers, dates, and proper names are the most common error types — always verify these manually. If accuracy is critical (legal, financial, medical contexts), treat AI extraction as a first draft that requires human review.

Use these verification prompts after any critical extraction:

- `"Check your extraction above against the original text. Did you miss any [names/dates/amounts]?"`
- `"List anything in your extraction that you were uncertain about or that required an inference."`
- `"If any field says 'not stated', confirm that this is correct by re-reading the relevant part of the source text."`

---

> ### 🟧 Module 3 — Reflection Questions
>
> 1. Which extraction type (entity, sentiment, summary, pattern) is most relevant to your current work?
> 2. After Try It 3A, did the AI miss or misattribute any information? What would you add to the prompt to catch that error?
> 3. How would you use the chained extraction technique (Try It 3E) on a document you regularly work with?
> 4. What is one specific recurring document in your work — a weekly report, email chain, or meeting note — where this extraction approach would save meaningful time?

---

## Module 4: Custom GPTs and Gemini Gems

Custom GPTs (in ChatGPT) and Gems (in Gemini) allow you to create a personalised AI assistant with a permanent role, instructions, and context — without writing a single line of code. In this module you will build your own custom assistant step by step.

### 4.1 What Are Custom GPTs and Gems?

Both features solve the same problem: instead of explaining your context and preferences every time you open a new chat, you configure them once and the AI remembers them permanently for that assistant.

| Feature | Custom GPTs (ChatGPT) | Gems (Gemini) |
|---|---|---|
| **Where to find it** | ChatGPT menu → Explore GPTs → Create | Gemini → Gem manager (top menu or sidebar) |
| **What you configure** | Name, description, instructions, conversation starters, knowledge files, capabilities | Name, instructions, and conversation starters |
| **Can upload files?** | Yes — PDFs, documents, spreadsheets become a knowledge base | Limited — mainly instruction-based currently |
| **Can share publicly?** | Yes — publish to GPT Store | Yes — share link with others |
| **Access required** | ChatGPT Plus/Pro subscription | Free with Google account (in supported regions) |

> 🟦 **Claude Projects — the equivalent feature on Claude**
>
> Claude does not use the "Custom GPT" or "Gem" terminology, but **Claude Projects** serves the same purpose.
>
> Go to **claude.ai → Projects** in the left sidebar → Create a new project. In a Project, you can write a permanent system prompt (called "Project Instructions"), upload knowledge files, and all conversations within the project inherit these instructions automatically. Claude Projects is available on free and paid accounts.

---

### 4.2 What to Put in Your Custom Instructions

| Component | What to write | Example |
|---|---|---|
| **Identity** | Who the AI is | *"You are Alex, a strategic communications assistant specialised in B2B technology."* |
| **Audience** | Who the user is | *"The user is a senior marketing manager at a mid-sized SaaS company."* |
| **Default behaviour** | How to approach every task | *"Always ask one clarifying question before starting. Default to concise, direct outputs."* |
| **Constraints** | What to always avoid | *"Never use jargon without defining it. Never write more than 400 words unless asked."* |
| **Format defaults** | Preferred output structure | *"Default to bullet points for lists, bold for key terms, and a one-sentence summary at the top."* |

---

### 4.3 Step-by-Step: Creating a Custom GPT in ChatGPT

You will build a **"Meeting Summary Assistant"** that turns rough notes into polished summaries.

> ### 🟪 Step 1 — Open the GPT Builder
> 1. Go to [chat.openai.com](https://chat.openai.com) and sign in.
> 2. In the left sidebar, click on your username or the menu icon.
> 3. Select **"My GPTs"** or click **"Explore GPTs."**
> 4. Click the green **"Create"** button in the top right.
> 5. You will see a split screen: the GPT Builder chat on the left, and a preview on the right.

> ### 🟪 Step 2 — Name and describe your GPT
> 1. Click the **"Configure"** tab at the top.
> 2. **Name:** `Meeting Summary Pro`
> 3. **Description:** `Turns rough meeting notes into structured, professional summaries with action items.`

> ### 🟪 Step 3 — Write your instructions
> In the **"Instructions"** box, paste the following:
> ```
> You are Meeting Summary Pro, a specialist assistant for transforming rough
> meeting notes into polished professional summaries. When the user pastes
> meeting notes, always produce output in this exact structure:
> (1) Meeting Overview (2 sentences max)
> (2) Key Decisions (bullet list)
> (3) Action Items as a table with columns: Owner, Task, Deadline
> (4) Open Questions (bullet list)
> (5) Next Meeting (date and purpose if mentioned)
>
> If information for a section is not in the notes, write "Not mentioned"
> rather than leaving it blank. Always use past tense for decisions and
> present tense for action items. Ask the user if they want a version
> formatted for email before producing the final summary.
> ```

> ### 🟪 Step 4 — Add conversation starters
> In the **"Conversation starters"** section, add:
> - `Summarise these meeting notes: [paste your notes]`
> - `Convert this to an email-ready summary: [paste your notes]`
> - `Extract only the action items from these notes: [paste your notes]`

> ### 🟪 Step 5 — Configure capabilities and save
> 1. Under **"Capabilities,"** keep **"Web Search"** enabled if you want it to look up referenced topics.
> 2. Click **"Save"** in the top right.
> 3. Choose **"Only me"** for private use, or **"Anyone with the link"** to share.

---

> ### 🟩 Try It 4A — Test your Custom GPT
> **Platform:** Your new Custom GPT "Meeting Summary Pro" in ChatGPT
>
> **Prompt to use:**
> ```
> Paste these rough notes: "Call with Priya and James - 45 mins - agreed to
> push launch to March 15, James to update the website copy by end of week,
> Priya checking with design team on banner ads, budget still TBC waiting
> for finance sign off, next call Thursday 2pm, open issue: do we need
> legal review of terms page before launch?"
> ```
>
> **What to observe:** Your Custom GPT should return a perfectly structured summary in the exact format you specified — every time, without you needing to repeat the instructions. Compare this to pasting the same notes into regular ChatGPT without instructions.

---

### 4.4 Step-by-Step: Creating a Gem in Gemini

You will build a **"Competitor Intelligence Analyst"** Gem.

> ### 🟪 Step 1 — Access Gem Manager
> 1. Go to [gemini.google.com](https://gemini.google.com) and sign in.
> 2. Look for **"Gem manager"** in the left sidebar or click the menu icon at the top.
> 3. Click **"New Gem"** (or the + button).

> ### 🟪 Step 2 — Name and write instructions
> **Name:** `Competitor Intelligence Analyst`
>
> In the instructions box, paste:
> ```
> You are a competitive intelligence analyst supporting a marketing strategy
> team. When the user names a company or product, do the following:
> (1) Provide a 3-sentence overview of what the company/product does.
> (2) List their top 3 apparent strengths based on public positioning.
> (3) List their top 3 apparent weaknesses or gaps.
> (4) Suggest 2 positioning angles our company could use to differentiate.
>
> Always note if your information may be outdated and recommend the user
> verify with current sources. Keep all outputs to under 350 words unless
> asked for more.
> ```

> ### 🟪 Step 3 — Add conversation starters and save
> Add these conversation starters:
> - `Analyse this competitor: [Company name]`
> - `Compare [Company A] and [Company B] for me`
> - `What are the weaknesses in [Company]'s market positioning?`
>
> Click **"Save."** Your Gem appears in the left sidebar under **"My Gems."**

---

> ### 🟩 Try It 4B — Test your Competitor Intelligence Gem
> **Platform:** Your new Gem "Competitor Intelligence Analyst" in Gemini
>
> **Prompt to use:**
> ```
> Analyse this competitor: Notion
> ```
>
> **What to observe:** Your Gem should return a structured competitive analysis using the format you specified. Compare the output to asking the same question in a standard Gemini conversation. The structure and analytical focus should be significantly sharper.

---

### 4.5 Step-by-Step: Creating a Claude Project

> ### 🟪 Step 1 — Create a new Project
> 1. Go to [claude.ai](https://claude.ai) and sign in.
> 2. In the left sidebar, click **"Projects."**
> 3. Click **"Create Project."**
> 4. Name it: `Proposal Writing Assistant`

> ### 🟪 Step 2 — Write Project Instructions
> Click **"Edit Project Instructions"** and paste:
> ```
> You are a specialist proposal writing assistant for a professional
> services consultancy. Your job is to help write, refine, and improve
> client proposals. Always:
> (1) Start by asking for the client name, project scope, and budget range
>     if not provided.
> (2) Use formal but engaging language appropriate for C-suite readers.
> (3) Structure proposals with: Executive Summary, Understanding of Need,
>     Proposed Approach, Team and Expertise, Timeline, Investment (pricing),
>     Next Steps.
> (4) Never include pricing specifics unless the user provides them.
> (5) Ask the user to confirm the tone before writing the full proposal:
>     formal, consultative, or relationship-led.
> ```

> ### 🟪 Step 3 — Upload knowledge files *(optional but powerful)*
> In the Project sidebar, look for **"Add content"** or **"Upload files."**
>
> Useful files to upload: past proposals, a list of services and pricing tiers, client case studies, your style guide. Claude will reference these files in every conversation within this project.

> ### 🟪 Step 4 — Start using your Project
> Click **"New conversation"** within the project. Try:
> ```
> I need to write a proposal for a logistics company that wants a 6-month
> digital transformation strategy. Budget is approximately $180,000.
> ```

---

### 4.6 Choosing the Right Custom Assistant for the Right Task

| Use case | Best platform | Why |
|---|---|---|
| Document drafting (proposals, reports, emails) | Claude Projects | Superior instruction-following for long-form structured writing |
| Customer-facing chatbot or public GPT | Custom GPT (ChatGPT) | GPT Store exposure, capability to add web search and file uploads |
| Research and competitive intelligence | Gemini Gem | Access to more current information; Google ecosystem integration |
| Consistent internal tool for a team | Custom GPT or Claude Project | Both offer shareable links; Claude Projects has strong file referencing |
| Multi-step data or process workflows | Custom GPT with file upload | GPT file analysis capability with code interpreter |
| Personal productivity assistant | Claude Project | Persistent instructions + file knowledge base is highly versatile |

---

### 4.7 Writing Effective Custom Instructions: Common Mistakes

> 🟥 **The 5 most common custom instruction mistakes**
>
> 1. **Too vague** — *"Be helpful and professional"* tells the AI nothing specific. Name the exact behaviours, formats, and decisions you want.
> 2. **No output format specified** — Always define the default structure. If you do not, the AI invents one each time.
> 3. **Contradictory instructions** — *"Be concise but comprehensive"* conflicts. Choose one or specify when each applies.
> 4. **Forgetting the audience** — Tell the AI who will be reading the outputs. This shapes vocabulary, depth, and tone.
> 5. **Never testing edge cases** — After setting up, test with an unusual input. Find the gaps in your instructions before relying on the assistant for real work.

---

> ### 🟩 Try It 4C — Stress-test your custom assistant
> **Platform:** Any of your three new custom assistants
>
> Send an input that is deliberately incomplete or unusual:
> - **Meeting Summary Pro:** `"summarise: quick call, we decided stuff, john will do things."`
> - **Competitor Gem:** `"analyse: my company."`
> - **Proposal Assistant:** `"write a proposal"` *(nothing else)*
>
> **What to observe:** Does the assistant ask clarifying questions as instructed? Does it default to a sensible format? Where does it break down? This tells you exactly what to add or fix in your instructions.

---

> ### 🟧 Module 4 — Reflection Questions
>
> 1. Which custom assistant use case is most immediately relevant to your work: proposal writing, meeting summaries, competitive research, or something else entirely?
> 2. After testing your custom assistant with incomplete input (Try It 4C), what did you add or change in your instructions?
> 3. What is a repetitive task in your role that could be turned into a custom assistant? Write the first draft of its instructions in 3–4 sentences.
> 4. What are the risks of over-relying on a custom assistant that has fixed instructions? When should you go back to a blank conversation instead?

---

## Lab Summary, Cheat Sheet, and Next Steps

### Module-by-Module Key Takeaways

| Module | The most important thing to remember |
|---|---|
| **1 — Customizing for Platforms** | ChatGPT rewards explicit structure; Claude rewards numbered instructions and nuance; Gemini rewards recency-focused, context-rich prompts. Match the prompt to the platform. |
| **2 — Optimizing Prompts** | CRAFT (Context, Role, Action, Format, Tone) is your pre-flight checklist. Running through it before any important prompt prevents 80% of weak-output problems. |
| **3 — Information Extraction** | The four-part formula (Source, Target, Format, Handling) turns messy text into structured data. Chain extraction steps for complex documents. Always verify numbers and names. |
| **4 — Custom GPTs and Gems** | One hour of setup saves hours of re-prompting. Always specify: identity, audience, default behaviour, constraints, and format. Test with edge cases before relying on it. |

---

### The Application Prompt Engineering Master Formula

```
PLATFORM: [Choose the right platform for this task based on Module 1 guidance]

ROLE: You are [specific expert with relevant background and years of experience].

CONTEXT: [Background situation, what decision or output this is for, any constraints].

AUDIENCE: [Who will read or use this output — their role, expertise, and what they care about].

TASK: [Active verb] + [specific deliverable] + [scope].
      Example: "Analyse the three most significant risks and provide a mitigation for each."

FORMAT: [Structure: sections, bullet points, table, length, tone].

HANDLING UNCERTAINTY: If you are unsure about any specific detail, flag it rather than inventing it.

NEGATIVE CONSTRAINTS: Do NOT [1–2 specific things to avoid].
```

---

### Platform Quick-Reference Card

| Task type | Recommended platform | Key prompt addition |
|---|---|---|
| Long document analysis or drafting | Claude | `"Analyse in sections. Flag uncertainty. Follow this exact structure: [list sections]"` |
| Creative or marketing content | ChatGPT | `"You are a [creative role]. Write for [audience]. Tone: [specific tone]."` |
| Research with recent information | Gemini | `"Use the most current available information. Focus on developments in the past 12 months."` |
| Structured data extraction | ChatGPT or Claude | `"Extract as a table with columns: [list columns]. Write 'not stated' for missing fields."` |
| Step-by-step complex reasoning | Claude | `"Think through this step by step. Show your reasoning before your conclusion."` |
| Competitive or market intelligence | Gemini | `"You are a strategic analyst. Use current public information. Structure: strengths, weaknesses, opportunities."` |
| Template-based consistent output | Claude | `"Fill in this exact template: [paste template]. Do not add fields not in the template."` |
| Public-facing chatbot or tool | Custom GPT (ChatGPT) | Write detailed system instructions covering identity, tone, boundaries, and default format. |

---

### Extraction Prompt Templates

Save these as your reusable extraction starters:

**Template A — Entity extraction**
```
Extract all [people/dates/organisations/amounts/obligations] from the text
below. Present as a table with columns: [Column 1], [Column 2], [Column 3].
If a field is not mentioned, write "not stated".

Text: [paste text]
```

**Template B — Sentiment and theme analysis**
```
Analyse the text below and provide:
(1) Overall sentiment (positive/neutral/negative) with a score 1–5 and
    one-sentence justification.
(2) Top 3 positive themes (bullet list).
(3) Top 3 negative themes (bullet list).
(4) One recommended action based on this analysis.

Text: [paste text]
```

**Template C — Document summary for decision-making**
```
Read the following document and extract:
CORE ARGUMENT (1 sentence):
KEY EVIDENCE (3 bullets):
IMPLICATIONS FOR [YOUR ROLE] (2 bullets):
UNCERTAINTIES OR GAPS (1 bullet):
RECOMMENDED ACTION (1 sentence):

Document: [paste document]
```

---

### Custom Assistant Quick-Setup Guide

| Platform | Where to go | Five essential instruction elements |
|---|---|---|
| **Custom GPT (ChatGPT)** | ChatGPT → Explore GPTs → Create → Configure tab | Identity + Audience + Default behaviour + Constraints + Format defaults |
| **Gemini Gem** | Gemini → Gem Manager → New Gem | Role + Task scope + Output format + Tone + What to flag/avoid |
| **Claude Project** | Claude → Projects → Create Project → Project Instructions | Role + Audience + Format defaults + Clarifying question behaviour + Constraints |

---

### Five-Day Practice Plan

| Day | Focus | Activity |
|---|---|---|
| **Day 1** | Platform customization | Take one prompt you use regularly and write three versions — one optimised for ChatGPT, one for Claude, one for Gemini. Run all three and compare. |
| **Day 2** | CRAFT check | Before sending your next five prompts at work, run them through the CRAFT checklist. Add any missing element and note the difference in output quality. |
| **Day 3** | Extraction | Take a real email thread, meeting note, or short report from your work. Run the entity extraction template and the sentiment template on it. |
| **Day 4** | Build a custom assistant | Create one Custom GPT, Gem, or Claude Project for a recurring task in your role using the five-element framework. Test with three different inputs. |
| **Day 5** | Stress-test and refine | Send deliberately incomplete or unusual inputs to your new custom assistant. Identify two gaps in your instructions and fix them. Share with one colleague. |

---

### Where to Go Next

- **GPT Store (ChatGPT)** — Explore examples of well-built Custom GPTs in your industry and use them as instruction inspiration.
- **Claude Projects** — Try uploading relevant documents for a team or client-specific project and see how it changes the quality of assistance.
- **Gemini + Google Drive** — Link Gemini to Google Drive and Docs to extract and summarise documents you already have in your workspace.
- **Combine labs** — Use the Advanced Prompt Engineering techniques (persona patterns, chain-of-thought, SPACE framework) inside your Custom GPT or Claude Project instructions for a particularly powerful combination.

---

## Glossary of Key Terms

| Term | Plain-language definition |
|---|---|
| **LLM** | Large Language Model — the AI technology behind ChatGPT, Claude, and Gemini. |
| **Prompt** | The message or instruction you send to an AI chatbot. |
| **Prompt optimization** | The process of refining a prompt to get better, more reliable, and more useful outputs. |
| **CRAFT framework** | Context, Role, Action, Format, Tone — a checklist for building effective prompts. |
| **Information extraction** | Using AI to pull specific, structured facts or patterns from unstructured text. |
| **Entity extraction** | Pulling out specific named items: people, dates, organisations, amounts, locations. |
| **Sentiment analysis** | Identifying the emotional tone (positive, negative, neutral) of a piece of text. |
| **Chained extraction** | A multi-step extraction process where each step builds on the results of the previous one. |
| **Custom GPT** | A personalised AI assistant built on ChatGPT with permanent instructions and capabilities. |
| **Gem** | Gemini's version of a personalised AI assistant with permanent instructions. |
| **Claude Project** | Claude's feature for permanent instructions and knowledge files that apply across conversations. |
| **Context window** | The amount of text an AI can hold in working memory during a single conversation. |
| **System prompt / Project instructions** | Permanent instructions set by the user that shape every conversation with a custom assistant. |
| **Guardrails** | Built-in safety rules that prevent AI from producing harmful or inappropriate content. |
| **Negative constraint** | An instruction telling the AI what NOT to do, used to avoid default unwanted behaviours. |

---

## Contributing

Found a better prompt? Want to add a module? PRs are welcome. Please keep exercises platform-agnostic (ChatGPT / Claude / Gemini) and suitable for non-technical learners.

## License

This lab guide is released under the [MIT License](LICENSE). Free to use, adapt, and share.
