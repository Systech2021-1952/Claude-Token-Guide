## CLAUDE TOKEN USAGE GUIDE

## What Is a Token?

A token is the basic unit of text processed by AI models. Tokens are not the same as

words—they are smaller pieces of text.

## Approximate Conversion

| Content | Approximation |
| -----   | ----- | 
| 1 token | ~4 English characters |
| 1 token | ~¾ of an English word
| 100 tokens | ~75 words |
| 1,000 tokens | ~750 words (approximately 1.5 pages) |

Note: Languages such as Tamil, Hindi, Japanese, and Chinese typically consume more tokens per word than English.


## Claude Context Window

The context window is the maximum number of tokens Claude can remember and process within a single conversation.

## Supported Models

| Model | Context Window |
|---|---|
|Claude 3.5 Haiku | 200,000 tokens |
|Claude 3.5 Sonnet | 200,000 tokens |
|Claude 3 Opus |  200,000 token |
| Claude 4 Sonnet | 200,000 tokens |
| Claude 3.7 Sonnet | 200,000 tokens |

## What Does 200,000 Tokens Mean?

## Approximately:

- 500 pages of text
- Hundreds of code files
- Multiple PDFs
- Long conversations

## What Counts Toward Token Usage?

Claude charges for both input and output tokens.

## Input Tokens

These include everything you send:

- Your prompt

- Previous conversation history

- System prompts (API)

- Attached documents

- Pasted code

- Images

## Output Tokens

These include everything Claude generates:

- Explanations

- Code

- Tables

- Lists

- Generated text
  
Both input and output tokens contribute to usage and billing.
----------

# Image Token Cost
Images use a fixed token cost rather than word-based tokenization.

| Image Size | Approximate Tokens |
|---|---|
| Small (<200 × 200 px) | ~300
| Medium | ~1,000–1,500 |
| Large (1000 × 1000 px or larger) | ~1,500–3,000 |

## Best Practice

Resize large images before uploading whenever high resolution isn't required.
----------

## API Pricing (Approximate)

| Model | Input (Per 1M Tokens)  | Output (Per 1M Tokens)  |
| --- | --- | --- |
| Claude 3.5 Haiku  | $0.80  | $4.00 |
| Claude 3.5 Sonnet | $3.00 | $15.00 |
| Claude 3 Opus | $15.00 | $75.00 |
| Claude 3.7 Sonnet | $3.00 | $15.00 |

## Claude.ai Pro

- Flat subscription (~\$20/month)
- No per-token billing within normal usage limits
----------

## Token Limits Per Response

| Limit | Approximate Value |
|----- | ----- |
| Maximum Input | Up to context window limit |
| Maximum Output | ~8,192 tokens (Haiku/Sonnet) |
| Extended Output | Up to ~32K tokens (select models) |

If Claude stops mid-response, simply ask:
- Continue
- Keep going
----------

## How the Context Window Works
### Every message becomes part of the conversation memory
### Example:

You: 
500 tokens

Claude: 
800 tokens

You: 
300 tokens

Claude: 
600 tokens


Running Total = 2,200 tokens


## CLAUDE TOKEN USAGE GUIDE

As conversations become longer:

- Previous messages remain in memory

- Total token usage increases

- Less room remains for future responses

## What Happens When the Context Window Is Full?

Once the context limit is reached:

- Older conversation history is removed first

- Earlier instructions may be forgotten

- Responses can become less consistent

- Large codebases and lengthy documents accelerate context exhaustion

## Recommended Solution

## Start a new conversation whenever switching topics or after completing a major task.

## Token Optimization Tips

## 1. Write Clear, Concise Prompts

## Instead of:

Can you please help me understand...

## Write:

Explain X in three bullet points.


## CLAUDE TOKEN USAGE GUIDE

## 2. Use Bullet Points

Structured prompts require fewer tokens than long paragraphs and are easier for Claude to interpret.

## Example:

- \- Summarize this article

- \- Maximum 150 words

- \- Focus on key findings

## Task:

## 3. Specify Response Length

## Examples:

- In 100 words

- Maximum five bullet points

- One paragraph

- Short explanation

This reduces unnecessary output tokens.

## 4. Share Only Relevant Content

Avoid pasting an entire document if only one section requires analysis.

## 5. Start New Chats Regularly

Old conversation history silently consumes context.

Separate different projects into different conversations whenever possible.

## 6. Use System Prompts (API)


## CLAUDE TOKEN USAGE GUIDE

If you're using the API, place repeated instructions in the system prompt rather than repeating them in every request.

## 7. Compress Long Conversations

Ask Claude to summarize the discussion.

Example:

Summarize this conversation in 200 words.

Then begin a new conversation using only that summary.

## Token Estimates

Content

Tweet (280 characters)

Instagram caption

800-word blog post

One A4 page

100 lines of code

One PDF page

This guide

Approximate Tokens

~70

~100–150

~1,100

~500

~700–1,000

~400–600

~1,200

## Token Counting Tools

Useful tools for measuring token usage:


## CLAUDE TOKEN USAGE GUIDE

- Anthropic Tokenizer — tokenize.anthropic.com

- Anthropic API — Returns usage.input_tokens and usage.output_tokens

- Claude.ai — Token usage available in conversation details and settings

## Best Practices

- Keep prompts concise and specific.

- Use bullet points whenever possible.

- Set a desired response length.

- Avoid repeating information Claude already has.

- Start new conversations for unrelated tasks.

- Summarize long discussions before continuing.

- Choose Haiku for simple tasks to reduce API costs.

- Reserve Sonnet or Opus for complex reasoning and coding tasks.

## Mental Model

Think of Claude's context window as a whiteboard.

Every message written on the board takes up space. As more information is added, the board gradually fills up. Once it's full, Claude begins erasing the oldest content to make room for new information.

The more focused and concise your conversation is, the more effectively Claude can use its available context.
