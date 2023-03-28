# Multilingual-Question-Answering

### Instructions:
- You can run train any model using ipynb file as it is.
- If you want to only test the model then use the evaluation script. change the
only model name in the evaluation.ipynb file.<br>
### Dataset Creation Files:
- Translation using <a href="https://huggingface.co/facebook/mbart-large-50-one-to-many-mmt">mbart-large-50-one-to-many-translation model</a>.<br>
File Name: Translation_code/squad_traslated_using_mbart.ipynb
- Translation using googletrans<br>
File Name: Translation_code/tydiqa_traslated_using_googletrans.ipynb
- Extracted telugu and bengali translations from
ai4bharat/IndicQuestionGeneration:<br>
File Name: Translation_code/squad-context-only.ipynb
- Extracted question translation from ai4bharat/IndicQuestionGeneration:<br>
File Name: Translation_code/squad-que-translate.ipynb<br>
### Datasets:
1) Tydiqa
2) Squad (only english)
3) <a href="https://huggingface.co/datasets/Gautam9595/Squad_Translated">Squad_mbart_translated</a>: 8139 questions of the squad dataset are translated
into telugu and bengali language using the mbart model.
4) <a href = "https://huggingface.co/datasets/krinal214/squad_ben_tel_context">Squad_ben_tel_context</a>: Keep only those question-answer pairs in which the answer is in context.
5) <a href="https://huggingface.co/datasets/krinal214/squad_ben_tel_que_only">Squad_ben_tel_que_only</a>: Used completely translated dataset of squad into bengali and telugu, then replace the translated questions with original questions in the original dataset.
6) <a href="https://huggingface.co/datasets/krinal214/tydiqa_ben_tel">Tydiqa_ben_tel</a>: 20k questions are translated into bengali and telugu each from different languages of the tydiqa dataset using googletrans.<br>

### Base Case:
- Filename: bert-all-tydiqa-only.ipynb<br>
Dataset: tydiqa<br>
Additional Dataset: None<br>
Best Model: bert-base-multilingual-cased<br>
Model: <a href="https://huggingface.co/krinal214/bert-all">bert-all</a><br>
### Additional Cases:
1) Filename: bert-all-tydiqa+squad.ipynb<br>
Dataset: tydiqa<br>
Additional Dataset: squad (english only - original)<br>
Model: <a href="https://huggingface.co/krinal214/augmented">augmented</a><br>
2) Filename: bert-all-tydiqa+tydiqa_que-translation.ipynb<br>
Dataset: tydiqa<br>
Additional Dataset: tydiqa_que-translation (20k questions of tydiqa are
translated into both bengali and telugu using googletrans)<br>
Model: <a href="https://huggingface.co/krinal214/bert-all-translated">bert-all-translated</a><br>
3) Filename: bert-all-tydiqa+squad_translated_using_mbart.ipynb<br>
Dataset: tydiqa<br>
Additional Dataset: Translated Squad (Only questions are translated into
telugu and bengali using mbart)<br>
Model: krinal214/augmented_Squad_Translated<br>
(link: https://huggingface.co/krinal214/augmented_Squad_Translated )<br>
4) Filename: bert-all-tydiqa+squad+squad_que.ipynb<br>
Dataset: tydiqa<br>
Additional Dataset: Squad (english only - original) + Translated Squad (Only
questions are translated into telugu and bengali)<br>
Best Model: krinal214/bert-all-squad_que_translated<br>
(link: https://huggingface.co/krinal214/bert-all-squad_que_translated )<br>
5) Filename: bert-all-tydiqa+squad+squad_context.ipynb<br>
Dataset: tydiqa<br>
Additional Dataset: Squad (english only - original) + Translated Squad (Used
translated data of squad from hugging face)<br>
Best Model: krinal214/bert-all-squad_ben_tel_context<br>
(link: https://huggingface.co/krinal214/bert-all-squad_ben_tel_context )<br>
6) Filename: bert-all-tydiqa+squad+squad_que+squad_context.ipynb<br>
Dataset: tydiqa<br>
Additional Dataset: Squad (english only - original) + Translated Squad (Only
questions are translated into telugu and bengali) +Translated Squad (Used
translated data of squad from hugging face)<br>
Best Model: krinal214/bert-all-squad_all_translated<br>
(link: https://huggingface.co/krinal214/bert-all-squad_all_translated )
