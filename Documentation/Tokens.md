# 📊 Token Consumption (Fireball Design v1.2)

Fireball Design v1.2 is designed to generate complete, production-ready interfaces. While the prompt itself is relatively compact, the total token consumption becomes significantly larger because modern LLMs resend the conversation history at every turn.

If the AI reasons in multiple steps, a typical generation consumes **around 20,000 tokens** in total.

## Example

| Step | Content | Approximate Tokens |
|------|---------|-------------------:|
| **Turn 1** | User request + system instructions | ≥100 |
| **Turn 1** | Generated HTML + CSS + JavaScript | ≥2,000 |
| **Turn 2** | Previous conversation resent as context | ≥2,000 |
| **Turn 2** | Assistant response being generated | ≥200 |
| **Additional reasoning** | Internal reasoning, revisions, planning, and context accumulation | ~15,700 |
| **Estimated Total** | Complete generation | **≈20,000 tokens** |

## Why so many tokens?

Large Language Models don't only read the latest message.

At each new conversation turn, they receive:

- the original user request;
- system instructions;
- previous messages;
- the entire generated website;
- any additional context accumulated during the conversation.

As the generated website becomes larger, every new iteration requires rereading more content, which increases token usage rapidly.

For this reason, a complete website generation with Fireball Design v1.2 typically reaches **around 20k tokens** when the model performs multi-step reasoning before producing the final result.

> **Note**
>
> The values above are estimates, not fixed limits. Actual token usage depends on the model, the complexity of the request, the size of the generated code, and the amount of conversation history included in the context.
