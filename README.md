# AI Web Developer

The [CodeGen paper](https://arxiv.org/abs/2203.13474) trained & released code generation models of various sizes (up to 16.1B parameters), focusing primarily on python code.

I found that the fastest & smallest multi-language model would get confused between programming languages, so wanted to fine-tune it to focus on a specific language.

I took the [smallest model (350M parameters)](https://huggingface.co/Salesforce/codegen-350M-multi) and fine-tuned it twice:
 - on HTML from [The Stack](https://huggingface.co/datasets/bigcode/the-stack)
 - on CSS from [The Stack](https://huggingface.co/datasets/bigcode/the-stack)

This model is an auto regressive transformer that predicts the next token.

The first model generates the HTML, which is then feed into the CSS model to generate the styling.

Try out generating a website here:
<a target="_blank" href="https://colab.research.google.com/github/alecsharpie/thiswebsitedoesnotexist/blob/main/notebooks/Generate_Website.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>


See the fine-tuning code here:
<a target="_blank" href="https://colab.research.google.com/github/alecsharpie/thiswebsitedoesnotexist/blob/main/notebooks/Finetune_CodeGen_Transformer.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
