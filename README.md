we can use LLM model such as Chatgpt, hyperclova etc.
But we should focus on how to solve a problem in terms of business.
So, Im studying what the difference is between MS Azure and Palatir AIP based on the situation that we want to use LLM with our own data.

I'd like tell you a few things before I go into detail. "fine-tunig" for LLM  is not best way to apply your business.
It requires long time and cost and It is not necessary good performance of model. because Almost all data in your company is unstructed and doesn't have any rules that AI can understand.

## (MS Azure) Cognitive Search + GPT
MS has GPT model license for business. It means If you want to ensure your data is secure, you can't avoid to use MS Azure.
And make sure MS doesn't provide "fine-tuning" of GPT anymore. But they suggest new way use GPT on your own data.
It's a GPT with Congnitive Search service.
what format your data is? you name it. It accepts any type of data format such as ppt, pdf, database, etc.
That's why many company are interested in Azure OpenAI service.

### Overall process of Azure OpenAI
(https://techcommunity.microsoft.com/t5/azure-ai-services-blog/revolutionize-your-enterprise-data-with-chatgpt-next-gen-apps-w/ba-p/3762087)
1. User ask a question
2. Orchestrator give Cognitive Search query and Cognitive Search return appreciate Knowledge.
3. Orchestrator give Prompt+Knowledge Azure OpenAI and OpenAI return response.

### Cognitive Search
The main point of Cognitive search is that they process your data before you use GPT. we call it "indexing".
After we do "indexing" beforehand, we can search it faster and effectively.
</br></br>
## (Palantir) Ontology + LLM + Tools
Palantir dosen't focus on only LLM with your data. They consider LLM is one of Tools for your business.
They has different aspect of using LLM based on your data, combining "Ontology" and LLM.
"Ontology" is similiar with digital twin. they said "Ontology is that give your data rules and It makes your company connect all teams and do more things than only use LLM.
By integrating ontologies with LLMs, we can create highly customized AI applications tailored to specific decision-making contexts. 
This combination allows AI systems to harness both structured and unstructured knowledge, leading to a more comprehensive understanding of a given domain.
Ontologies provide the necessary context for LLMs, allowing them to disambiguate terms and accurately interpret the meaning behind language. 
For instance, the word “apple” could refer to a fruit or a technology company, depending on the context. 
An ontology can provide this context, enabling the LLM to understand which meaning is appropriate in a given situation.


