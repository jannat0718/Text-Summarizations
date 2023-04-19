## Extractive and Abstractive Text-Summarizations

**Text summarization** is the process of automatically generating a shortened version of a given document or text. In this era of big data and information overload, text summarization has become an essential tool for processing and presenting information in a concise and meaningful way. There are two main approaches to text summarization: extractive and abstractive.


**Abstractive summarization**, on the other hand, involves generating a summary that may contain new phrases and sentences not present in the original text. The process requires a deeper understanding of the text's content and context, as the summary is generated by rephrasing and restructuring the original text while preserving its meaning. Abstractive summarization is more challenging than extractive summarization but can produce more concise and readable summaries.

## **Extractive Summarization of Web Articles Using Transformer-based Models**

**Extractive summarization** involves selecting the most important sentences or phrases from the original text and presenting them as a summary. The summary consists of verbatim sentences or phrases extracted from the original text, and the goal is to maintain the coherence and meaning of the original content. Extractive summarization is relatively straightforward and requires less linguistic knowledge than abstractive summarization. This report presents a project that aims to perform extractive summarization of web articles using a pre-trained Transformer model available through the Hugging Face library. The process begins with scraping the content from the target URL, preprocessing the data, and chunking the text into smaller segments. The pre-trained summarization pipeline is then applied to each chunk to generate an extractive summary.

**Objective:**

The objective of this project is to develop a workflow for extractive summarization of web articles, allowing users to quickly understand the most important information without reading the entire article.

**Detailed Step-by-Process:**

  a. Installed required packages, including transformers, BeautifulSoup, requests, and other optional libraries for parsing web pages.
  
  b. Imported necessary libraries, such as the summarization pipeline from transformers, BeautifulSoup, and requests.
  
  c. Provided a target URL to scrape the content.
  
  d. Requested the website content using the requests library.
  
  e. Parsed the webpage content with BeautifulSoup, extracting headings and text.
  
  f. Removed labels from the extracted text and join the text into a single string.
  
  g. Modifird punctuations and split the article into sentences.
  
  h. Defined a maximum chunk size and chunk the text into smaller segments.
  
  i. Loaded the summarization pipeline from the pre-trained Transformer model.
  
  j. Applied the summarization pipeline to each chunk, generating a summary with a specified maximum and minimum length.
  
  k. Joined the separate summaries to create a comprehensive extractive summary.
  
**Results and Analysis:**

The project successfully extracted and summarized a web article using the pre-trained Transformer model. The model provided an 80-word summary for each chunk, which was combined to create a comprehensive extractive summary. The generated summary focused on the most relevant and important information from the original article.

**Optimization:**

To optimize the performance of the summarization model, the chunk size, minimum length, and maximum length parameters can be adjusted based on the specific content and summarization requirements. Additionally, domain-specific fine-tuning of the pre-trained model can improve its performance on specific types of articles.

In conclusion, this project demonstrates the feasibility of using a pre-trained Transformer model for extractive summarization of web articles. By scraping, preprocessing, and chunking the article content, the summarization pipeline was applied to produce a summary that captured the most important information from the original text. Further optimization can be performed to tailor the summarization process to specific needs and improve the model's performance on domain-specific content.


## **Abstractive Summarization Using the PEGASUS-XSUM model and PEGASUS-large model:**


Performance Comparison:
Compared to abstractive summarization, the extractive summarization approach preserves the original wording and structure of the source text. While this may provide more accurate representations of the content, it may not be as concise as an abstractive summary, which paraphrases the content.

	Installed Pytorch, SentencePiece, and Transformer for Pegasus Model instantiation, Tokenization & detokenization process.

	Acquired and extracted text using BeautifulSoup and requests functions.

	Performed tokenization of the extracted text using PegasusTokenizer library with pre-trained Pegasus-xsum and Pegasus-large model. The token contains a unique Id for each word and an attention mask value. The attention mask specifies the direction of token generation during the unmasking phase.

	Using PegasusForConditionalGeneration library with Pegasus-xsum and Pegasus-large model to instantiate the model for transfer learning.

	Fed the tokens into the model to generate the abstractive summarization. 

	Pegasus-xsum model generated only a statement of summary where Pegasus-large model generated 5-8 sentences of comprehensive summary.

	As the Pegasus model is based on Gap-sentence or masking based there is no overlapping of an exact sentence in the result rather it's more like a paraphrasing of text.

**Citations:**

1. H. P. Luhn, "The Automatic Creation of Literature Abstracts," IBM Journal of Research and Development, vol. 2, no. 2, pp. 159-165, 1958. Link

2. R. Nallapati, F. Zhai, and B. Zhou, "Summarunner: A Recurrent Neural Network based Sequence Model for Extractive Summarization of Documents," in Proceedings of the 54th Annual Meeting of the Association for Computational Linguistics, Berlin, Germany, 2016, pp. 214-223. Link

3. R. Rush, S. Chopra, and J. Weston, "A Neural Attention Model for Abstractive Sentence Summarization," in Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing, Lisbon, Portugal, 2015, pp. 379-389. Link

4. S. Karami and A. Sarkar, "A Review of Text Summarization Techniques," Artificial Intelligence Review, vol. 53, no. 4, pp. 2371-2404, 2020. Link

5. S. S. Barik, P. R. Tripathy, and A. K. Rath, "A Comparative Study of Extractive and Abstractive Text Summarization Techniques," International Journal of Computer Applications, vol. 179, no. 46, pp. 6-13, 2018. Link

6. Zhang, J., Zhao, Y., Saleh, M., & Liu, P. J. (2020). PEGASUS: Pre-training with Extracted Gap-sentences for Abstractive Summarization. Retrieved from https://arxiv.org/abs/1912.08777
