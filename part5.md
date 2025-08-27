# Comparison between models
- When using distilbert for retrieveing context, the LLM model out-performs our "Classical" model by a significant amount.
It seems that distilbert doesn't handle well the raw context that our retriever retrieves, while the LLM can extract from the context useful information easily.

- However when distilbert gets more useful context (literal or pragmatic answer) it performs similarly to the llm.

- I did observe much improvement when getting the conversation history as context: The llm out-preformed even the distilbert, when given the pragmatic/literal context.


# Theory of Mind
- It seems that with history and additional world knowledge about the subject, the llm can infer user intentions and answer accordingly in some cases, but this phenomenon isn't widely appearent. In the experiment there are many cases where retrieved context confuse the llm about what the user actually asked.