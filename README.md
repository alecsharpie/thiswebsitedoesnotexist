# AI Web Developer

The [https://arxiv.org/abs/2203.13474](CodeGen paper) trained & released code generation models of various sizes (up to 16.1B parameters), focusing primarily on python code.

I found that the fastest & smallest multi-language model would get confused between programming languages, so wanted to fine-tune it to focus on a specific language.

I took the [https://huggingface.co/Salesforce/codegen-350M-multi](smallest model (350M parameters)) and fine-tuned it twice:
 - on HTML from [https://huggingface.co/datasets/bigcode/the-stack](The Stack)
 - on CSS from [https://huggingface.co/datasets/bigcode/the-stack](The Stack)

This model is an auto regressive transformer that predicts the next token.

The first model generates the HTML, which is then feed into the CSS model to generate the styling.

Try out generating a website here:
https://colab.research.google.com/drive/1TqRh-kGw_kJr6LTWNZjyjvF2GzXy6E9w?usp=sharing


See the fine-tuning code here:
