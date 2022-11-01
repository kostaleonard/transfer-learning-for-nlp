# Chapter 1: What is transfer learning?

Transfer learning allows you to apply knowledge gained from one set of tasks
and/or domains to another set of tasks and/or domains.

## Overview of representative NLP tasks

* Part of speech tagging
* Named entity recognition
* Document classification
* Sentiment analysis (can be seen as a special case of document classification)
* Automatic summarization
* Machine translation
* Question answering
* Chatbot
* Speech recognition
* Language modeling
* Document parsing

## Understanding NLP in the context of AI

"Based on [the advances achieved in AI by taking inspiration from evolution],
it seems flawed that for each new task, language, or application domain, the
supervised learning process has traditionally been repeated from scratch."

## A brief history of NLP advances

Embeddings are a form of implicit transfer learning, the result of which is to
reduce the amount of data and thereby compute required to achieve good
performance on a downstream task.

Although word-level models have been prominent in the past, character-level
models are more robust to natural language because humans express themselves
using a wide range of emoticons, never-before-seen words, and deliberate or
accidental misspellings.

## Transfer learning in computer vision

We can learn some useful lessons for NLP transfer learning by studying transfer
learning in computer vision. Computer vision models frequently use pretrained
ImageNet models as a base. Then one of two techniques is performed:

1. Feature extraction. The pretrained network outputs from the penultimate
layer are used as the inputs of another model, typically either a shallow
network or a traditional ML model like SVM.
2. Fine-tuning. A portion of the last layers in the pretrained model are frozen
and progressively retrained, from deeper to shallower, on the new target task.
This strategy works because the shallower layers capture more general features
such as edges or color maps, whereas deeper layers capture task-specific
combinations of general features. Heuristically, if the data available for the
target task is large, the whole network can be fine-tuned. If only a small
amount of data is available, only the last layers are fine-tuned, and the
fine-tuning process is dependent on the similarity of the source and target
tasks. If the tasks are very similar, the whole pretrained model can be
fine-tuned as is. If the tasks are different, some of the last layers of the
pretrained model may need to be discarded.
