# :o: Cognitive Services on Azure sp20-516-243 David Drummond

## Introduction

Cognitive services on Azure provides AI technologies to those with little AI understanding. It is the umbrella service for all of the pretrained models in Azure's library. These services provide valuable resources for those who need vanilla AI service applications without much custom tuning. They provide API or SDK plugins for REST API, Python, .NET, Node.js,and Go. With this broad spectrum of native and plugin application, it gives developers relevant tools to incorporate these services into their applications. [[Documentation]](<https://docs.microsoft.com/en-us/azure/cognitive-services/face/index>)

## Applications

As cognitive services is an umbrella service, there are different categories of developer tools within this service. This includes decision tools, language tools, speech tools, and vision tools. Not all tools are available in all regions. [[Documentation]](<https://azure.microsoft.com/en-us/global-infrastructure/services/?products=all>). 

### Decision

Decision tools enable stakeholders to automate data analysis for a variety of applications including anomoly detection, content moderation, and personalizing. This can provide service for both end-user and developer to scale businesses and automate menial work.  

#### Anomoly Detector

Anomoly detector is a decision feature that provides automated detection of outstanding data patterns. Specifically, this tool works to monitor any time-series data. This feature is in preview phase, therefore access is limited. 

Azure suggests this tool can be applied to business metrics, IoT data stream, or any time timestamps are applied to data. The algorithm looks for seasonality, spikes, and dips in the data. [[Video](<https://channel9.msdn.com/Shows/AI-Show/Introducing-Azure-Anomaly-Detector?WT.mc_id=ai-c9-niner>)] This tool has been used by Microsoft in their Microsoft 365 product management for several years and recently made the tool available to developers. 

The anomoly service [API](<https://docs.microsoft.com/en-us/azure/cognitive-services/anomaly-detector/>) kits are accessible through the Azure documentation.  


|Account                  |INSTANCE	PRICE                    |
|---                      |---                               |
|Free- Web/Container      |	20000 transactions free per month|
|Standard - Web/Container |	$0.157 per 1,000 transactions    |

<https://azure.microsoft.com/en-us/services/cognitive-services/anomaly-detector/>

#### Content Moderator

Content moderator serves as a gatekeeper for content on user generated content. It will detect offensive content in text, videos, and images. Most, but not all servers have this feature installed. This feature is most often used with user generated content platforms. This tool scans uploaded images, texts, and videos and tags potentiallly objectionable content. This content can then be passed to a moderator for human review. The human review updates the model with his or her feedback 

|Account  |	Transactions per Second (TPS)	| Features        |	Price              |
|---      |---                            |---              |---                 |
|Free     |	1 TPS	                        | Moderate, Review| N/A                |
|         |                               |                 |                    |
|Standard	|10 TPS	                        |Moderate, Review |	0-1M transactions - $1 per 1,000 transactions|
|         |                              |                  |1M-5M transactions - $0.75 per 1,000 transactions|
|         |                              |                  |5M-10M transactions - $0.60 per 1,000 transactions|
|         |                              |                  |10M+ transactions - $0.40 per 1,000 transactions|

<https://azure.microsoft.com/en-us/services/cognitive-services/content-moderator/>

#### Personalizer

Personalizer is a ready to use, SDK for user recomendations on end user expereinces. This service has limited server rollout. 

The algorithm works by the developer assigning user actions to a algorithmic reward system. If the computer correctly identifies the users action, it is rewarded, else it recieves not reward and adjusts the algorithm. 

|Account|Price|Storage|
|---|---|---|
|Free|50,000 transactions free /month               | 10 GB                     |
|     |                                              |                          |
|Paid|First 1M transactions $1 per 1000 transactions| 0 GB/1M transactions/month|
|    |Next 9M transaction $0.35 per 1000 transactions|                          |
|    |Next 90M transaction $0.20 per 1000 transactions|                         |  |    |Above 100M transactions $0.05 per 1000 transactions|                       |
|    |Above 100M transactions $0.05 per 1000 transactions|                       |

<https://docs.microsoft.com/en-us/azure/cognitive-services/personalizer/what-is-personalizer>

<https://azure.microsoft.com/en-us/services/cognitive-services/personalizer/>

### Language

The language application package aims to add natural language processing tools to developers in the form of API and SDK. 

#### Immersive Reader

Immersive reader is a preview only service to add AI text to speech integration for accessibility services. In preview, this feature is free and pricing out of preview is unavailable. The SDK packs for this projects are limited to Swift, node.js, and ASP.NET Core. The main features of immersive reader are text to speech, focused reading windows, visual reading cues, and syllable-word breakdown. 

<https://docs.microsoft.com/en-us/azure/cognitive-services/immersive-reader/>

<https://azure.microsoft.com/en-us/services/cognitive-services/immersive-reader/>

#### Language Understanding

Language Understanding is a pretrained natural language processor. It is available through SDK using C#, Python, and JavaScript. It is additionally available using REST in all REST compatible languages. Free versions of language understanding can process typed language; whereas, the paid version can process both typed and spoken language. Language understanding can be applied to bot services or IoT control. 

|INSTANCE|TRANSACTIONS PER SECOND (TPS)|FEATURES|PRICE|
|---     |---                          |---     |---|
|Free Web/Container|	5 TPS |	Text Requests|10,000 transactions free per month|
|Standard|50 TPS|Text Requests|$1.50 per 1000 transactions|
|||Speech Requests|$5.50 per 1000 transactions|

<https://azure.microsoft.com/en-us/services/cognitive-services/language-understanding-intelligent-service/>

#### QnA Maker

QnA Maker uses Knowledge base databases to create a chat bot. It can be customized to different levels of formality. It allows for additional processes to be added over time. It supports C#, Python, and JavaScript. For knowledge base integreation it supports cURL and Postman.

|INSTANCE|TRANSACTIONS PER SECOND (TPS)|LIMITATIONS|PRICE|
|---     |---                          |---     |---|
|Free Web/Container|	3 TPS |	Up to 1MB each document|
|                 |         |Up to 100 transactions per minute|
|                 |         |Up to 50,000 transactions per month|
|                 |         |3 managed documents free per month|
||||
|Standard|3 TPS|Up to 100 transactions per minute|$10 for unlimited managed documents|

<https://docs.microsoft.com/en-us/azure/cognitive-services/QnAMaker/quickstarts/get-answer-from-knowledge-base-using-url-tool?pivots=url-test-tool-curl>

<https://azure.microsoft.com/en-us/services/cognitive-services/qna-maker/>

#### Text Analytics

Text analytics aims to provide broad range text analytic service in SDK packaging. The key features are sentiment analysis, key phrases extraction, named entities extraction and language determination. There is SDK available for C#, Python, Node.js, Go, and Ruby. It provides easy integration to Power BI and Flask. 

|INSTANCE|FEATURES|PRICE|
|---|---|---|
|Free    |Sentiment Analysis      |N/A|
|        |Key Phrase Extraction   ||
|        |Language Detection      ||
|        |Named Entity Recognition||
|        |                        ||
|Standard|Sentiment Analysis|0-500,000 text records: $2 per 1,000 text records|
|        |Key Phrase Extraction|0.5M-2.5M text records: $1 per 1,000 text records|
|        |Language Detection| 2.5M-10.0M text records: $0.50 per 1,000 text records|
|        |Named Entity Recognition|10M+ text record: $0.25 per 1,000 text records |

<https://azure.microsoft.com/en-us/services/cognitive-services/text-analytics/>

#### Translator Text

The translator text API provides neural translator services for developer integration. It is available in C# and REST API. Azure marketing tools indicate that it is useful for increasing research text data, detecting input language, bilingual dictionary tools, on device translation, and custom trained translation. 

|INSTANCE|FEATURES|PRICE|
|---|---|---|
|Free|Standard Translation|2M Characters Free|
|    |-Text Translation||
|    |-Language Detection||
|    |-Bilingual Dictionary||
|    |-Transliteration||
|    |Custom Translation||
|    |-Training||
||||
|S1  |Standard Translation|Standard|
|    |-Text Translation|- $ 10 per million characters|
|    |-Language Detection||
|    |-Bilingual Dictionary|Custom|
|    |-Transliteration|- $ 40 per million chars of custom translation|
|    |Custom Translation|- $ 10 per million source + target chars of training data (max. $ 300/training)|

<https://azure.microsoft.com/en-us/services/cognitive-services/translator-text-api/>

### Speech

Speech packages adds additional natural language processing tools to developers for spoken language. Azure provides API access through REST API as well as SDK in C++, C#, Java, JavaScript, Objective-C, and Python. 

#### Speech to Text

The speech to text tool uses neural network speech recognition algorthms to convert audiofiles to plaintext. Its applications include accesibility for the deaf and hard of hearing and domain specific vocabulary transcription.

|Instance|Features|Price|
|---|---|---|
|Free|Standard|5 audio hours free per month|
|   |Custom|5 audio hours free per month. 1 model free per month|
|   |      |                                                    |
|Standard|Standard|$1 per audio hour|
|        |Custom|$1.40 per audio hour. Endpoint hosting: $0.0538 per model per hour|


<https://azure.microsoft.com/en-us/services/cognitive-services/speech-to-text/>

#### Text to Speech

Azure Text to Speech is a neural network text to speech tool that is meant to provide life-like voice synthesis to applications. Azure provides both access to pretrained models and the abiltiy to create unique voice models for specific applications.This can be used in place of immersive reader for accessibility features meant for blind individuals. 


|Instance|Features|Price|
|---|---|---|
|Free|Standard|5M characters free per month|
|   |Neural|0.5M characters free per month|
|   |Custom|5M characters free per month. Endpoint hosting: 1 model free per month|
|   |     |                              |
|Standard|Standard|$4 per 1M characters|
|   |Neural|$16 per 1M characters|
|   |Custom| $6 per 1M characters. Endpoint hosting: $0.0537 per model per hour |
|   |Custom Neural|Real-time synthesis: $24 per 1M characters. Endpoint hosting: $4.04 per model per hour. Long audio creation: $100 per 1M characters|

<https://azure.microsoft.com/en-us/services/cognitive-services/text-to-speech/>

#### Speech Translation

Speech translation provides real time speech translation tools to applications. Unlike speech to text and text to speech, speech translation is only cloud-based and will not operate on edge devices. 

|Instance|Price|
|---|---|
|Free|5 audio hours free per month|
|Standard|$2.50 per audio hour|

<https://azure.microsoft.com/en-us/services/cognitive-services/speech-translation/>

#### Speaker Recognition

Speaker recognition is a preview only tool available to developers. It is in early preview so the SDK's available for the other speech services are not ready currently. It is accessible through REST API. The service detects the speaker of an audio clip and names the entity, given that the entity has been captured previously. This can be used for multispeaker transcription services. As a preview, it is currently a free service.

<https://azure.microsoft.com/en-us/services/cognitive-services/speaker-recognition/>

### Vision

Azure Vision is an umbrella brand for the products using computer vision and image recogniton software. It includes the services Computer Vision, Custom Vision, Face, Form Recognizer, and Ink Recognizer.

#### Computer Vision

Computer vision is a pretrained computer vision model that can detect more than 10,000 ibjects. It can be trun in the cloud or in edge containers. Azure claims this service can be applied to robotic process automation, digital asset management, or to accesibillity features for the blind. The pricing strategy for computer vision is based on the object being detected. However, Azure provides 20 free transactions per minute. The full pricing detail can be found [here.](<https://azure.microsoft.com/en-us/pricing/details/cognitive-services/computer-vision/>) There is SDK available in .NET, Python, Java, Node.js, and Go.

<https://azure.microsoft.com/en-us/services/cognitive-services/computer-vision/>

#### Custom Vision

Custom vision allows fevelopers to custom train a computer vision model. It is optimized for small data inputs and large differences in objects. Azure warns that it is not optimal for quality assurance. The model can be exported for offline use. There is SDK available in .NET, Python, Java, Node.js, and Go. 

|Instance|Transactions per Second|Features|Price|
|---|---|---|---|
|Free|2 TPS|Upload, training, and prediction transactions. Up to 2 projects. Up to 1 hour training per month|5,000 training images free per project. 10,000 predictions per month|
|Standard|10 TPS|Upload and prediction transactions. Up to 100 projects|$2 per 1,000 transactions|
|        |      |Training|$20 per compute hour|
|        |      |Image Storage|$0.70 per 1000 images|

<https://azure.microsoft.com/en-us/services/cognitive-services/custom-vision-service/>

#### Face

The Face API is a facial detection and analysis software. It identifies the face and extracts features such as head pose, gender, age, emotion, facial hair, and eye wear detection. It can be used to verify identity and find similar faces or identical faces.  There is SDK available in .NET, Python, Java, Node.js, and Go.

|Instance|Tranactions per Minute|Price|
|---|---|---|
|Free|20 TPM|30,000 transactions free per month|
|    |      |                                   |
|Standard|600 TPS|0-1M transactions - $1 per 1,000 transactions|
|       |       |1M-5M transactions - $0.80 per 1,000 transactions|
|       |       |5M-100M transactions - $0.60 per 1,000 transactions|
|       |       |100M+ transactions - $0.40 per 1,000 transactions |
|Face Storage|  |$0.01 per 1,000 faces per month|

<https://azure.microsoft.com/en-us/services/cognitive-services/face/>

#### Form Recognizer

Form recognizer takes images or PDFs and autopopulates their contents into custom or prebuilt forms. This may include pictures receipts, invoices, bills, or legal forms. The Form Recognizer can use supervised or unsupervised learning to populate the custom forms. It is only available using REST API or .NET SDK. 

|Instance|Document Type|Price|
|---|---|---|
|Free| |0-500 pages Free per Month|
|Standard|Custom|$25 per 1000 pages|
|         |Pre-Built|$5 per 1000 pages|

<https://azure.microsoft.com/en-us/services/cognitive-services/form-recognizer/>

#### Ink Recognizer

Ink Recognizer is a handwritting recognition software. It can be used with pen and paper interactions or digital handwriting. Azure suggests applying this service to notetaking, form-filling, content search, and documentation annotation. 

|Instance|Price|
|---|---|
|Free|2000 transactions free per month|
|Standard| 	$2 per 1,000 transactions|

<https://azure.microsoft.com/en-us/services/cognitive-services/ink-recognizer/>


