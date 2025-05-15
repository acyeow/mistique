_The majority of the code is from a [tutorial by pixegami](https://www.youtube.com/watch?v=ldFONBo2CR0&t=1694s). The purpose of this code is my personal exploration and learning about AWS CDK, Retrival Augmented Generation and Next.js application development._

# mistique

mistique allows users to ask questions about the Mistral7B reserach paper thorugh a Retrival Augmented Generation (RAG) pipeline.

This application uses ChromaDB to create a vector database, which will be queried to find relevant information to the prompt. To create the embeddings for the vector database, Amazon Bedrock embeddings are used and cosine similarity is used to compute the similarity between the prompt embedding and embeddings saved to the ChromaDB. This functionality is wrapped in a FastAPI endpoint which has been deployed as an AWS Lambda function. AWS CDK was used to provison resources for support this functionality. The frontend of this application was created using Next.js and deployed to Vercel.

### FastAPI Endpoint Docs

[FastAPI Endpoint Docs](https://oodh4zow7mwurrycf663bs7uwm0twcjp.lambda-url.us-east-1.on.aws/docs)

### Deployed Application

[Vercel Application](https://deploy-rag-to-aws-mu.vercel.app/)
