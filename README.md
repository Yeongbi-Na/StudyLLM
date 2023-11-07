we can use LLM model such as Chatgpt, hyperclova etc.
But we should focus on how to solve a problem in terms of business.
So, Im studying what the difference is between MS Azure and Palatir AIP based on the situation that we want to use LLM with our own data.

## MS Azure Cognitive Search + GPT"
MS has GPT model license for business. It means If you want to ensure your data is secure, you can't avoid to use MS Azure.
And make sure MS doesn't provide "fine-tuning" of GPT anymore. But they suggest new way use GPT on your own data.
It's a GPT with Congnitive Search service.
what format your data is? you name it. It accept any format of data such as ppt, pdf, database, etc.
That's why many company are interested in Azure OpenAI service.

### Overall process of Azure OpenAI
(https://techcommunity.microsoft.com/t5/azure-ai-services-blog/revolutionize-your-enterprise-data-with-chatgpt-next-gen-apps-w/ba-p/3762087)

1. User ask a question
2. Orchestrator give Cognitive Search query and Cognitive Search return appreciate Knowledge.
3. Orchestrator give Prompt+Knowledge Azure OpenAI and OpenAI return response.



### Cognitive Search
The main point of Cognitive search is that they process your data before you use GPT. we call it "indexing".
the process is below.


임베딩 인덱싱의 주요 단계와 예시는 다음과 같습니다:
1. 임베딩 생성: 텍스트 데이터를 임베딩으로 변환하는 과정을 수행합니다. 이 단계는 주로 사전 훈련된 모델(예: Word2Vec, BERT)을 사용하여 수행됩니다.
예시:
	• 문장 "나는 고양이를 좋아해"를 BERT를 사용하여 임베딩으로 변환합니다.
2. 인덱스 생성: 생성된 임베딩을 인덱스 구조에 저장합니다. 가장 일반적으로 사용되는 인덱스 구조는 역 인덱스(inverted index)입니다. 
3. 역 인덱스는 각 임베딩 벡터와 해당 원본 데이터(예: 문서) 간의 매핑을 유지하는 데이터 구조입니다.
예시:
	• "고양이"라는 단어의 임베딩을 역 인덱스에 저장하고, 해당 임베딩과 연결된 모든 문서의 ID 목록을 유지합니다.
4. 검색 쿼리 처리: 사용자가 검색 쿼리를 제출하면, 검색 엔진은 해당 쿼리를 임베딩으로 변환합니다.
예시:
	• 사용자가 "강아지"라는 검색 쿼리를 제출하면, "강아지"의 임베딩을 생성합니다.
5. 유사성 계산: 검색 엔진은 검색 쿼리 임베딩과 데이터베이스 내의 모든 임베딩 간의 유사성을 계산합니다. 
6. 일반적으로 코사인 유사도(cosine similarity) 또는 유클리디안 거리 등을 사용하여 임베딩 간의 유사성을 측정합니다.
예시:
	• 검색 쿼리 임베딩과 데이터베이스 내의 문서 임베딩 간의 코사인 유사도를 계산합니다.
7. 결과 랭킹: 검색 결과를 해당 검색 쿼리와의 유사성에 따라 랭킹합니다. 가장 관련성이 높은 결과가 먼저 표시됩니다.
예시:
	• 가장 높은 유사성을 갖는 문서가 상위에 표시됩니다.
8. 검색 결과 반환: 랭킹된 결과를 사용자에게 반환하고, 검색된 데이터의 일부 또는 전체를 표시합니다.
예시:
사용자에게 "강아지"와 관련된 문서 목록을 제공합니다.![Uploading image.png…]()



