# NLP_experiments

I am using an NLP code that uses embeddings in Glove to summarize a Wall Street Journal article that I know very well.
This is in the notebook codeA_0.ipynb where 'A' stands for advanced.
I use the code in this site:
https://thecleverprogrammer.com/2020/08/24/summarize-text-with-machine-learning/

For comparison, I am doing the same exercise but this time using a python library that does tokenization.
This is in the notebook code_0.ipynb
I use the code in this site:
https://thecleverprogrammer.com/2020/12/31/text-summarization-with-python/


The data set is a pdf article from wsj converted to text using https://pdftotext.com/

source - at this url:
https://www.wsj.com/articles/the-day-coronavirus-nearly-broke-the-financial-markets-11589982288

The advanced code does an amazing job of summarization.

So, even without understanding the implementation details, it is possible to use NLP & achieve practical results.

Perhaps one could optimize the pipeline: in my case, I just converted pdf to text, and then pasted the text output in one cellzinof the jupyter notebook.

This experiment is intended as a starting point. Even so I can envisage using it on many articles I have collected and it will help me summarizing better.

# Next steps

Remove  newline (\n) characters in the text file as follows:
sed ':a;N;$!ba;s/\n/ /g' foo.txt > foo_output.txt
see https://www.linkedin.com/posts/joseph-pareti-b603a9a_google-machinetranslation-preprocessing-activity-6855540890677608448-Txup/

Use T5 Transformer from John Snow Lab as shown here: https://github.com/JohnSnowLabs/spark-nlp-workshop/blob/master/tutorials/streamlit_notebooks/T5TRANSFORMER.ipynb

The latter has been implemented in notebook codeA_JSL.ipynb using code from https://github.com/JohnSnowLabs/spark-nlp-workshop/blob/master/tutorials/streamlit_notebooks/T5TRANSFORMER.ipynb

Howver, comparing codeA_0.ipynb and codeA_JSL.ipynb shows that T5 summarizes the text even further, but lots of the article informtation and insights are lost

