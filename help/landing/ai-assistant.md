---
title: AI Assistant for Adobe Experience Platform
description: Learn how to use AI Assistant to navigate and understand Experience Platform and Real-Time Customer Data Platform concepts, and usage information about your objects.
badge: Beta
hide: true
hidefromtoc: true
exl-id: 8be1c222-3ccd-4a41-978e-33ac9b730f8c
---
# AI Assistant for Adobe Experience Platform

>[!NOTE]
>
>AI Assistant for Adobe Experience Platform is currently in Beta. The feature and documentation are subject to change.

AI Assistant is a UI feature that you can use to navigate and understand Adobe Experience Platform and Real-Time Customer Data Platform concepts and usage information about your objects.

You can query AI Assistant for information such as:

* Guidance on how to perform tasks pertaining to data and audiences.
* Statuses and metrics of the existing data objects in your organization.
* Use case examples and nuances to better understand your data objects, including attributes, audiences, dataflows, datasets, destinations, schemas, and sources.

Read the guide below to learn how you can use AI Assistant to help navigate and understand your Experience Platform and Real-Time CDP workflows.

>[!BEGINSHADEBOX]

**How does AI Assistant work?**

AI Assistant responds to your submitted questions by querying a database and then translating data from the database into a human-readable answer.

This internal representation of underlying data is also known as the Knowledge Graph - a comprehensive web of concepts, data, and metadata for a given answer. 

The Knowledge Graph consists of sub-graphs that are referenced whenever queries submitted:

* Customer usage data.
* Customer usage data across various meta-stores.
* Experience League documentation.

There are two classes of questions to consider before querying AI Assistant:

* **Concept Questions**: Concept questions are about Adobe concepts related to data or audiences. Some examples of concept questions include:
  * What is the difference between batch and streaming segmentation?
  * Are there industry data models and how do I use them?
  * What is Real-Time CDP best used for?
* **Usage Questions**: Usage questions are about the data objects inside your organization. Some examples of usage questions include:
  * How many datasets do I have?
  * How many schema attributes have never been used?
  * Which audiences have been activated?

>[!ENDSHADEBOX]

## Objectives that you can accomplish with AI Assistant {#objectives}

You can use AI Assistant for objectives such as:

| Objective | Description | Example |
| --- | --- | --- |
| Learning concepts and continuing workflows | <ul><li>As a novice user, you can use AI Assistant to learn Real-Time CDP and Adobe Journey Optimizer concepts and onboard yourself to products and features that you are unfamiliar with.</li><li>As an experienced user, you can use AI Assistant to solve an edge case that may be blocking your workflow. |<ul><li>How do I set up a dashboard in Journey Analytics?</li><li>Tell me some use-cases for Real-Time CDP.</li></ul> |
| Troubleshooting | Use AI Assistant to learn how to debug basic errors that you may encounter in your workflow. | <ul><li>What does this error {ERROR_MESSAGE} mean?</li><li>Why am I not able to delete the audience named "Luma: Email Audience"?</li></ul> |
| Sandbox hygiene | Use AI Assistant to identify any duplicates or unused objects so you can efficiently maintain your sandbox. | <ul><li>Can you show me audiences that are similar?</li><li>Are there any schemas which do not have an associated dataset?</li></ul> |
| Value analysis | Use AI Assistant to identify your most used data objects and assess any performance indicators or find the most valuable data objects. | <ul><li>How many profiles are in our "Luma: Email Audience" segment definition?</li><li>When were audiences activated to Experience Cloud Audiences destination?</li></ul> |
| Search | Use AI Assistant to find supported Experience Platform objects such as audiences, datasets, destinations, schemas, and sources. | <ul><li>List the audiences containing "Luma" in the name that were created in the last quarter.</li><li>What attributes are in the "Luma: Custom Actions" XDM schema?</li></ul> |
| Impact analysis | Use AI Assistant to identify data objects that have been used in certain workflows so that you can assess the impact of any changes. | <ul><li>Which audiences use `homeAddress.city` in "Luma: PersonProfiles" schema?</li><li>Which datasets are the `consents.marketing.push.val` profile attribute stored in?</li></ul> |

## Access AI Assistant in the Experience Platform UI

To launch AI Assistant, select the **[!UICONTROL AI Assistant icon]** from the top header of the Experience Platform UI.

![The Experience Platform home page, with the AI Assistant icon selected and the AI Assistant interface open.](./images/ai-assistant/ai-assistant.png)

The AI Assistant interface appears, immediately providing you with information to get started. You can use the options provided under [!UICONTROL Ideas to get started] to answer questions and commands such as:

* [!UICONTROL Which of my audiences are activated?] 
* [!UICONTROL What is a schema?]
* [!UICONTROL Tell me some common use cases for Real-Time CDP]

## AI Assistant UI guide

>[!NOTE]
>
>The following workflow is an example that uses the experience event schema creation process to illustrate how you can use AI Assistant when using the Experience Platform UI.

Consider a use case in which you are creating a **Device Trade in Event Schema**. During the experience event schema creation process, you come across the `eventType` field. "At this point, you have the option to either exit your workflow and refer to the [basics of a schema composition](../xdm/schema/composition.md) documentation, or you can use AI Assistant to retrieve answers to your questions and find additional resources through the documentation links recommended by AI Assistant."

To begin, enter your question in the text box provided. In the example below, AI Assistant is provided the question: "**What is the eventType field in an ExperienceEvent schema?**"

![AI Assistant for Experience Platform with the following question prepared for querying: "What is the eventType field in an ExperienceEvent schema?](./images/ai-assistant/question.png)

AI Assistant then queries its knowledge base and computes an answer. After a few moments, AI Assistant returns an answer and related suggestions that you can use as follow up prompts.

![AI Assistant for Experience Platform with an answer to the previous query.](./images/ai-assistant/answer.png)

After receiving a response from AI Assistant, you can select from a number of options to decide how you want to proceed.

### AI Assistant features {#features}

This section outlines the different features of AI Assistant that you can use during your workflows on Experience Platform.

<!-- 
### Save your query {#save-your-query}

+++Select to view an example of how to save a query

To save your query, select the bookmark icon beside your question.

![Screenshot of a selected bookmark.](./images/ai-assistant/save-your-query.png)

To access your saved queries, select the bookmark icon below the input box, then select the query you would like to run.

![Screenshot of bookmark icon and a list of saved queries.](./images/ai-assistant/bookmarks.png)

+++ -->

### View data in your sandbox {#view-data-in-your-sandbox}

Depending on your query, AI Assistant provides additional information pertaining to the data in your sandbox. To view how the response to your query applies to your particular sandbox, select **[!UICONTROL In your sandbox].** 

When viewing data pertaining to your sandbox, AI Assistant may provide direct links to specific UI pages that display your queried data.

+++Select to view example

In this example, AI Assistant returns additional information regarding the existing XDM schemas in your sandbox, including their total count and the five most commonly used fields.

![The "in your sandbox" dropdown window open, displaying additional information on your schemas.](./images/ai-assistant/in-your-sandbox.png)

+++

### View citations {#view-citations}

You can verify responses returned to you by AI Assistant by reviewing citations available with every answer.

+++Select to view an example of how to display sources

To view citations and validate AI Assistant's response, select **[!UICONTROL Show sources]**. 

![The AI Assistant response with "Show sources" selected.](./images/ai-assistant/show-sources.png)

AI Assistant updates the interface and provides you with links to documentation that corroborate the initial response. Additionally, when citations are enabled, AI Assistant updates the response to include footnotes to indicate the specific parts of the answer that reference the provided documentation. 

![A dropdown menu of the citations that AI Assistant provides for concept questions.](./images/ai-assistant/citations.png)

You can also use the queries that AI Assistant provides under **[!UICONTROL Related suggestions]** to further explore topics related to your original query.

![A list of queries provided by AI Assistant as related suggestions.](./images/ai-assistant/related-suggestions.png)

+++

### Usage data and visualization {#usage-data-and-visualization}

You must be in an active sandbox in order for AI Assistant to sufficiently respond to a question about your usage data.

+++Select to view an example of usage data questions and data visualization

In the example below, AI Assistant is asked the following query: **"Show me dataflows that were created using the Amazon S3 source"**, AI Assistant then responds with a table listing your dataflows and their corresponding IDs. To view the whole table of data, select the expand icon on the top right.

![Follow up question about usage data.](./images/ai-assistant/usage-data-question.png)

An expanded view of the table appears, providing you with a more comprehensive list of dataflows based on the parameters of your query.

![A view of the expanded table.](./images/ai-assistant/table.png)

When prompted with a usage data question, AI Assistant provides an explanation of how it computed the answer. In the example below, AI Assistant outlines the steps it took in order to identify the dataflows that were created using the [!DNL Amazon S3] source.

![Follow up question about segment definitions illustrating how AI Assistant computed the answer.](./images/ai-assistant/answer-explained.png)

You can also provide filters and modifications to your queries, and you can instruct AI Assistant to render its findings based on the filters that you include. For example, you can ask AI Assistant to show you a trend of the count of segment definitions in the order of their created date, remove segment definitions with zero total profiles, and use month names instead of integers when displaying the data.

+++

### Use auto-complete {#use-auto-complete}

You can use the autocomplete function to receive a list of data objects that exist in your sandbox. Autocomplete recommendations are available for the following domains: audiences, schemas, datasets, sources, and destinations.

+++Select to view an example of auto-complete

You can use autocomplete by including the plus symbol (**`+`**) in your query. As an alternative, you can also select the plus sign (**`+`**) located at the bottom of the text input box. A window appears with a list of recommended data objects from your sandbox.

![Example of auto-complete](./images/ai-assistant/autocomplete.png)

+++

### Use multi-turn {#use-multi-turn}

You can use AI Assistant's multi-turn capabilities to have a more natural conversation during your experience. AI Assistant is able to answer follow-up questions, given. that context can be inferred from an earlier interaction.

+++Select to view an example of multi-turn

In the example below, AI Assistant is first asked for the total number of dataflows and then is asked to list the 10 most recent dataflows.

![Example of multi-turn](./images/ai-assistant/multi-turn.png)

+++

## Provide feedback {#feedback}

You can provide feedback of your experience with AI Assistant using the options provided with answer.

To provide feedback, select either thumbs up, thumbs down, or a flag after receiving a response from the AI Assistant, and then input your feedback in the provided text box. 

![The feedback option in AI Assistant.](./images/ai-assistant/provide-feedback.png)


+++Select to view more examples

>[!BEGINTABS]

>[!TAB Thumbs up]

Select the thumbs up icon to provide feedback on what went well with your experience with the AI Assistant.

![The positive feedback window.](./images/ai-assistant/thumbs-up.png)

>[!TAB Thumbs down]

Select the thumbs down icon to provide feedback on what could be improved upon based on your experience with the AI Assistant. During this step, you can also provide specific comments regarding your experience. Feedback provided in the comments is reviewed daily.

![The negative feedback window.](./images/ai-assistant/thumbs-down.png)

>[!TAB Flag]

Select the flag icon to provide further reports on your experience using the AI Assistant.

![The report results window.](./images/ai-assistant/flag.png)

>[!ENDTABS]

+++

## Documentation {#documentation}

Currently, the documentation index covers Adobe Experience Platform (Real-Time CDP and Audiences). The index is updated periodically.

The documentation retrieval model is trained on Experience Platform (Real-Time CDP and Audiences). Questions outside the scope of Adobe Experience Platform such as, questions about other Adobe products like Adobe Target and the Creative Cloud suite cannot be answered.

## Usage data {#usage-date}

You can also ask AI Assistant questions about your usage data in the following domains: 

* Attributes
* Audiences
* Dataflows
* Datasets
* Destinations _(Questions regarding accounts and some questions about dataflow cannot be answered at this time.)_
* Schemas _(Questions regarding field groups cannot be answered at this time.)_
* Sources _(Questions regarding accounts cannot be answered at this time.)_

For usage data queries, answers may not reflect the current state of the UI. The data backing these questions is updated once every 24 hours. For example, changes that users make in Real-Time CDP during the daytime are synced with the data stores at night, and then they become available for user questions in the morning. Additionally, you will need to log into a sandbox to inquire about specific data related to objects like audiences, schemas, datasets, attributes, and destinations.

### Example usage data questions {#example-usage-data-questions}

+++Select to see a list of example usage data questions

Read the table below for examples of usage data questions and their respective use cases:

| Question type | Use case| Examples |
| --- | --- | --- | 
| Data lineage | Track usage of one or multiple objects across other Experience Platform objects | <ul><li>Which datasets use the "ACME schema" schema?</li><li>How many datasets have been ingested using the same schema?</li><li>Which datasets have been used in activated audiences?</li><li>List the schemas which have attributes used in activated audiences.</li><li>Show me the audiences that are activated to "ACME Destinations" and have more than 1000 profiles.</li><li>Show me the attributes which are used in the activated audiences which have been modified after Jan 2023.</li><li>What are the datasets ingested via "ACME Amazon S3" source?</li><li>Which dataflows are associated with "ACME Loyalty Dataflow"?</li><li>List the schemas that are related to activated audiences and were created in last 1 year.</li></ul> |
| Distribution and aggregations | Summary-based questions about Experience Platform object usage | <ul><li>What is the percentage of activated audiences?</li><li>How many fields are used in segmentation?</li><li>Which audiences are activated to the most number of destinations?</li><li>List duplicate audiences.</li><li>Show me the audiences activated to "ACME Destinations" and rank them by profile size.</li><li>What is the percentage of the audiences which have not been activated but have more than 100 profiles. Show me their names.</li><li>List the 3 source connectors ingesting data into my datasets.</li><li>List me the top 5 attributes used in activated audiences based on their occurrence.</li></ul> |
| Object lookup | Retrieve or access an Experience Platform object or it's properties. | <ul><li>Which datasets do not have any schema associated with them</li><li>List the attributes used for "ACME Audience"?</li><li>Give me the list of schemas which are profile enabled but have not been modified since their creation.</li><li>Which audiences have been modified in the last week?</li><li>List me the audiences which have the same segment definitions along with their creation date.</li><li>Which datasets are profile enabled and also include how many audiences have been created from each dataset.</li><li>Which source accounts are associated with dataset XYZ?</li><li>Show me the segment definition and modification date of "ACME Audience".</li></ul>|
| Object comparison | Identify duplicate audiences. | <ul><li>Based on their segment definition, list the audiences that are duplicates.</li><li>Which duplicate audiences are activated to "ACME Destinations".</li></ul> |

+++

## Phrasing your questions {#phrasing-your-questions}

You must phrase your questions to AI Assistant with clarity and context in order to get as accurate a response as a possible. Refer to the following list of tips for guidance on how to ask a clear question with context:

* State your task and/or question in a concise manner.
* Avoid ambiguous language or overly complex syntax to facilitate comprehension.
* Provide relevant context regarding your task and/or question as context can help AI Assistant generate more relevant responses.

Read the table below for further guidance on best practices to follow when asking questions to AI Assistant:

| Do | Example |
| --- | --- |
| <ul><li>Be specific about the object or information that you want to retrieve or analyze.</li><li>Try placing your data object names in quotes. If you only know a part of the object name, you may also specify that in the question.</li><li>Use [object auto-complete](./ui-guide.md#use-auto-complete) to help AI Assistant better understand the context of your query.</li></ul> | <ul><li>Which datasets use the "Luma - Loyalty" schema?</li><li>Show me the activated segments which have "Luma" in their names. Rank them by profile count.</li></ul> |
| <ul><li>Avoid ambiguity and use clear language</li><li>Use precise terminology to ensure better clarity in your query.</li><li>When asking questions regarding Adobe Experience Platform, try to use terminology specific to Experience Platform to improve relevance of responses.</li></ul> | <ul><li>How many profiles do I have in "ACME Audience".</li><li>Show me the top 5 XDM attributes used in activated audiences.</li></ul> |
| <ul><li>Provide context or specify a criteria to filter your results.</li><li>Use a filter criteria in the questions to limit the volume of data in the response.</li></ul> | <ul><li>Show me audiences that have not been activated and were created more than 6 months ago and have never been modified.</li><li>Show me audiences activated to "ACME Destination" and have more than 10000 profiles.</li></ul> |

{style="table-layout:auto"}

| Don't | Example |
| --- | --- |
| Use vague or ambiguous language. | <ul><li>Give me information about datasets.</li><li>How many users do I have in "ACME Audience"?</li><li>Show segments.</li><li>List attributes.</li></ul>|
| Make incomplete requests. | "Luma - Loyalty Dataset" |
| Assume knowledge without context. | <ul><li>Audiences in the last 6 months.</li><li>Build a query for me.</li></ul>|
| Formulate overly complex queries. | Provide a comprehensive analysis of data lineage across all objects and their dependencies. |
| Omit criteria or parameters. | Show me datasets. |

{style="table-layout:auto"}

## Additional information {#additional-information}

Refer to this section for additional information on the AI Assistant for Experience Platform.

### Caveats and limitations {#caveats-and-limitations}

The following section outlines current caveats and limitations to considers when using AI Assistant.

#### Limited small talk

You can engage in small talk with the AI Assistant, but this capacity is currently limited.

#### Capability questions

The AI Assistant may give an inaccurate impression of what it can do. It may answer the following types of questions incorrectly:

| Example question | Note |
| --- | --- |
| "Can you answer questions on {ENTITY}?" | As long as the AI Assistant is able to find a single page referencing a given entity in its index, then it will respond yes. |
| "Do you know **x** language?" | The AI Assistant currently only supports English, but may answer "yes" due to the underlying model being able to support it. |
| "Can you do...?" | The AI Assistant may answer yes, even though it cannot. |

## FAQ {#faq}

The following is a list of answers to frequently asked questions about AI Assistant.

### Is AI Assistant's information provided in real-time?

The data presented in AI Assistant responses is updated daily. This means that data in responses can be up to 24 hours older than the data that you may see on the Experience Platform user interface, at the time of the response.

### Which Adobe applications does AI Assistant support?

AI Assistant supports Adobe Experience Platform, Real-Time Customer Data Platform and Adobe Journey Optimizer concept questions. For data usage questions, AI Assistant currently only supports Real-Time CDP data objects.

### What are the capabilities of AI Assistant?

AI Assistant can address Adobe concept queries and can answer questions related to the usage of Experience Platform objects. (For example, "How many audiences are activated?").

### Can AI Assistant provide information about profile data?

No. AI Assistant does not have access to profile-level data.

### Will my personal information be utilized in AI Assistant's training data?

AI Assistant does not use personal information for training purposes. Do not provide any personal information about yourself (including your name or contact information) or any other parties to AI Assistant.