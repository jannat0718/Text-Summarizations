# Text-Summarizations-
End-to-end Extractive and Abstractive summarization of articles/blogs using Hugging Face pre-trained base Transformer libraries for learning and understaning purpose.

##**For Extractive Summarization:**

	Extracted Article or Blog from a given URL using BeautifulSoup and requests functions in Python.

	Chunked the text data for a maximum number of  500 Tokens.

	Loaded the  Summarization pipeline from the pre-trained base Transformer and passed each chunked text to produce one summary of 80 words for each chunk. After joining   all the separate summaries to generate a comprehensive summary.


##**Abstractive Summarization Using the PEGASUS-XSUM model and PEGASUS-large model:**

	Installed Pytorch, SentencePiece, and Transformer for Pegasus Model instantiation, Tokenization & detokenization process.

	Acquired and extracted text using BeautifulSoup and requests functions.

	Performed tokenization of the extracted text using PegasusTokenizer library with pre-trained Pegasus-xsum and Pegasus-large model. The token contains a unique Id for each word and an attention mask value. The attention mask specifies the direction of token generation during the unmasking phase.

	Using PegasusForConditionalGeneration library with Pegasus-xsum and Pegasus-large model to instantiate the model for transfer learning.

	Fed the tokens into the model to generate the abstractive summarization. 

	Pegasus-xsum model generated only a statement of summary where Pegasus-large model generated 5-8 sentences of comprehensive summary.

	As the Pegasus model is based on Gap-sentence or masking based there is no overlapping of an exact sentence in the result rather it's more like a paraphrasing of text.
