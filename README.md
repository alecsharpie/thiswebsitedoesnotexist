# AI Web Developer

The [CodeGen paper](https://arxiv.org/abs/2203.13474) & [Github Repo](https://github.com/salesforce/codegen) trained and released code generation models of various sizes (up to 16.1B parameters), focusing primarily on python code.

I found that the fastest & smallest multi-language model would get confused between programming languages, so wanted to fine-tune it to focus on a specific language.

I took the [smallest model (350M parameters)](https://huggingface.co/Salesforce/codegen-350M-multi) and fine-tuned it twice:
 - on HTML from [The Stack Dataset](https://huggingface.co/datasets/bigcode/the-stack), model card [350m_html](https://huggingface.co/alecsharpie/codegen_350m_html)
 - on CSS from [The Stack Dataset](https://huggingface.co/datasets/bigcode/the-stack), model card [350m_css](https://huggingface.co/alecsharpie/codegen_350m_css)

This model is an auto regressive transformer that predicts the next token.

The first model generates the HTML, which is then feed into the CSS model to generate the styling.

## Try out generating a website here:
<br>
<a target="_blank" href="https://colab.research.google.com/github/alecsharpie/thiswebsitedoesnotexist/blob/main/notebooks/Generate_Website.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>


## See the fine-tuning code here:
<br>
<a target="_blank" href="https://colab.research.google.com/github/alecsharpie/thiswebsitedoesnotexist/blob/main/notebooks/Finetune_CodeGen_Transformer.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
