# 1. Motivations and Contributions

## Motivations

- Need for pragmatic reasoning: Human communication often relies on understanding unspoken intentions and anticipating follow-up needs—think of someone asking, “Do you have a minute?”—where a good answer doesn’t just affirm time availability but prepares for a possible request 


- Limitations of existing QA datasets: Standard QA benchmarks mostly target literal, extractive answers and don't test whether systems can grasp what the asker really wants to know beyond the surface 

- Crowdsourcing quality issues: Traditional datasets suffer from incentive misalignment—workers may not produce rich conversational data unless the task incentivizes depth and engagement 


## Contributions

- Introduction of PRAGMATICQA: The first large-scale (6,873 QA pairs) open-domain, conversational QA dataset where answers include both literal and pragmatic content 


- Novel crowdsourcing framework: Workers choose topics of genuine interest and can participate both as learners and teachers, encouraging deeper engagement and richer conversation alignments 


- Pragmatic-focused evaluation metrics: In addition to accuracy, the authors propose metrics for evaluating pragmatic reasoning, naturalness, and faithfulness of answers 

- Empirical evidence of model gaps: Even models like Fusion-in-Decoder struggle to capture most pragmatic information present in human answers 


# 2. Why PRAGMATICQA Is Challenging and What Pragmatic Phenomena It Targets

## A challenging dataset because:

- Beyond literal answers: It requires not just a factual answer, but enriching it with contextually relevant, follow-up anticipating content—a higher-level conversational skill.

- Minimal literal-pragmatic overlap: Literal and pragmatic spans share very few words (on average ~4.4 words), making it hard for models relying on lexical similarity 

- Deep topic exploration: Conversations draw from ~16 HTML elements across 3 web pages on average—demonstrating rich, multi-document reasoning 


- High diversity: Questions range from simple yes/no (~22%) to complex factoid and narrative types; pragmatic spans serve various roles like answering follow-ups (41%) or steering the conversation forward (25%) 


## Pragmatic phenomena targeted:

- Implied intent and anticipatory context: Responding in ways that address what the questioner likely wants, not just what they asked.

- Engaging conversational utility: Including information that invites further questions or deepens understanding.

- Interest alignment and naturalness: Answers reflect conversational tone, flow, and anticipation in ways that literal extracts don’t.

# 3. Sample Conversations and How Pragmatic Answers Enrich Literal Ones

### Below are approximately five illustrative examples drawn from the dataset (based on the repository descriptions and Figure 5 of the paper). Each pairs a literal answer with a pragmatic version, showing how pragmatic augmentation enhances the response.

*Example 1:* “Is there water on Mars?”

*Literal:* Yes, there is water on Mars.

*Pragmatic:* Yes, but only in the form of ice caps near its poles. In fact, Mars is just one of 23 places where we have found water in the Solar System!

- Why it enriches: Anticipates “where?” and “in what form?”, gives engaging comparative context 

*Example 2:* “When had the first Zelda game been released?” (Figure 5)

*Literal:* It came out as early as 1986 in Japan and later in 1987 in the Western world.

*Pragmatic:* The Legend of Zelda was first released as early as 1986 in Japan and later to the western world in 1987. It was the first installment in the Zelda franchise and its success allowed the development of sequels, with nearly every game in the series influenced by it!

- Why it enriches: Adds historical context, significance, and franchise relevance, anticipating curiosity about what came next 

*Example 3:* "Whats the maximum range you can go with a Tesla model 3"

*Literal:* Tesla Model 3 has a range of approximately 260 miles.

*Pragmatic:* Tesla Model 3 goes about 260 miles on a charge—which means you can comfortably do a full workweek commute on one overnight charge. Plus, the wide Supercharger network makes long trips much more feasible.

- Why it enriches: Anticipates usability needs and addresses potential concerns about charging infrastructure.

*Example 4:* What vitamins do oranges have?

*Literal:* Oranges are high in vitamin C.

*Pragmatic:* Oranges are high in vitamin C, giving you about 70 mg per fruit—more than your daily requirement. As a bonus, they're also rich in fiber and hydrating—great for a healthy snack!

- Why it enriches: Goes beyond the nutrient fact to practical dietary advice.

*Example 5:* (Conversational guidance scenario)

Suppose someone asks about writing a good resume:

*Literal:* Your resume should be no more than two pages.

*Pragmatic:* Keep your resume within two pages—concise but impactful. Highlight your most recent and relevant roles first, use bullet points with measurable achievements, and tailor it to the job description to make your application stand out.

- Why it enriches: Moves from rule to actionable guidance.

## What These Illustrations Show

- Context-aware augmentation: Pragmatic answers address why the question matters, not just what the answer is.

- Conversational fluency: They mimic natural teacher-student or assistant-user interaction—engaging, informative, and smooth.

- Anticipation and engagement: Pragmatic responses often preempt follow-ups—covering "what next", "why it matters", or "how to use this information".

- Realistic supervision signals: Training on such enriched responses could guide models to be more helpful, not just factually correct.